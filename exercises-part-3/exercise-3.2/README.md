# Implementation of exercise 3.2

#### In order to run this app successfuly you need to have linked an ssh-key from your machine into your github settings for authentication, if you don not know how check [here](https://docs.github.com/en/authentication/connecting-to-github-with-ssh) for instructions.
#### Copy and paste only the url of the repo that you want to clone
#### You will also need you credentials in order to push your image once it is created successfuly.
___

In order to build the image you need to run the command below and make sure you have your ssh-key created and likned to you github account
```
docker build . -t dockerizing --build-arg SSH_PRIVATE_KEY="$(cat ~/.ssh/id_rsa)";
```

After succesfuly building the image you can run it with the command below:
```
docker run -it -v /var/run/docker.sock:/var/run/docker.sock dockerizing
```

## Shell file configuration
```sh
#!/bin/sh

printf "Starting the Dockerizing process\n"
read -p "Repository URL: " repo_url
basename=$(basename $repo_url)
repo_name=${basename%.*}
if [ ! -d "./$repo_name" ]; then
  printf "Cloning repo $repo_name...\n"
  git clone "$repo_url"
  status=$?
  printf "Status $status\n"
  if [[ "$status" == 0 ]]; then
    printf "Repository cloned \033[1;32mOK\033[0m!\n"

    printf "\033[96mDoes your Dockerfile exists?\033[0m\n"
    read -p "y (yes) / n (no): " answer1
    if [ $answer1 == "n" ]; then
      printf "Creating Dockerfile...\nYou will be able to edit your Dockerfile after entering the variables\n"
      read -p "FROM: " base
      read -p "EXPOSE: " port
      read -p "ENV variable (if non just write URL=http;//): " variable
      read -p "RUN commands: " commands
      read -p "Command CMD, in quotations: " cmd
      echo FROM $base $'\n\n'WORKDIR /usr/src/app $'\n\n'COPY . . $'\n\n'EXPOSE $port $'\n\n'ENV $variable $'\n\n'RUN $commands $'\n\n'CMD [ "$cmd" ] $'\n' >./$repo_name/Dockerfile
      nano ./$repo_name/Dockerfile
      printf "Dockerfile created, \033[1;32mOK\033[0m!\n"
    fi
    printf "\033[33mMAKE SURE YOUR DOCKERFILE IS CORRECT BEFORE CONTINUING\033[0m\n"
    read -p "Is your Dockerfile correct? y (yes): " answer2
    if [ $answer2 == "y" ]; then
      printf "Would you like to create a docker image?\n"
      read -p "y (yes) / n (no): " answer3
      if [ $answer3 == "y" ]; then
        printf "Give a tag to your image\n"
        read -p "Image name: " image
        printf "Creating image...\n"
        docker build ./$repo_name -t $image
        printf "\033[1;32mImage created!\033[0m\n"
      fi
      printf "Would you like to publish the image to Docker Hub?\n"
      read -p "y (yes) / n (no): " answer4
      if [ $answer4 == "y" ]; then
        read -p "Docker Hub username: " docker_user
        read -p "Docker Hub password: " password
        docker login -u $docker_user -p $password
        printf "Pushing image to Docker Hub...\n"
        docker tag $image $docker_user/$image
        docker push $docker_user/$image:latest
        printf "\033[1;32mImage has been pushed!\033[0m"
      fi
    fi
  else
    printf "\033[91mIncorrect github username or repo name\033[0m, \033[33mtry again or ctrl+c to exit\033[0m!\n"
    bash dockerizing.sh
  fi
else
  printf "Respository \033[1;31malready exists\033[0m! \033[33mtry again or ctrl+c to exit\033[0m.\n"
  bash dockerizing.sh
fi
```
___
## Dockerfile configuration
```docker
FROM ubuntu

ARG SSH_PRIVATE_KEY

WORKDIR /usr/src/app

# Update aptitude with new repo
RUN apt-get update
# Install software 
RUN apt-get install -y git

RUN apt-get install -y nano

RUN mkdir /root/.ssh/
# Copy over private key, and set permissions
# Warning! Anyone who gets their hands on this image will be able
# to retrieve this private key file from the corresponding image layer
RUN echo "${SSH_PRIVATE_KEY}" > /root/.ssh/id_rsa

RUN chmod 600 /root/.ssh/id_rsa

# Create known_hosts
RUN touch /root/.ssh/known_hosts

# Add bitbuckets key
# RUN ssh-keyscan -t rsa github.com >> /root/.ssh/known_hosts
RUN ssh-keyscan github.com >> /root/.ssh/known_hosts

RUN apt-get install docker.io -y

COPY . .

CMD [ "bash", "dockerizing.sh" ]
```
___