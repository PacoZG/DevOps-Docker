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