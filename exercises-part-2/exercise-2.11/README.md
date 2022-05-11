# Implementation of exercise 2.11
- The repository/project used for this exercise can be found at [pacoder](https://github.com/PacoZG/pacoder), we only need to copy the docker-compose, dockerfile and the nginx files to the root of the project and proceed with the steps below.
# Development environment
## docker-compose.dev file configuration
```yaml
version: '3.8'

services:
  pacoder_dev:
    image: pacoder_dev
    container_name: pacoder_dev
    build:
      context: .
      dockerfile: Dockerfile.dev
    command: npm start
    ports:
      - 3000:3000
    volumes:
      - ./:/usr/src/app
      - node_modules:/usr/src/app/node_modules 

volumes:
  node_modules:
```
___
## Dockerfile.dev file configuration
```docker
FROM node:16

WORKDIR /usr/src/app

COPY package* ./

RUN npm install
```
___

I named these files so that I can separate environments, we can run the compose file by running the following command on the terminal:
```
$ docker-compose -f docker-compose.dev.yml up
```
With this we can do a interactive development on which we can see the changes on the browser even when we are running the environment with a container. it can be open at http://localhost:3000

# Production environment with nginx

## docker-compose file configuration
```yaml
version: '3.8'

services:
  pacoder:
    image: pacoder
    container_name: pacoder
    build:
      context: .
      dockerfile: Dockerfile
    ports:
      - 3000:3000
  
  nginx:
    image: nginx
    container_name: nginx
    ports:
      - 80:80
    volumes:
      - ./nginx.conf:/etc/nginx/nginx.conf
```
## Dockerfile
```docker
FROM node:16

WORKDIR /usr/src/app

COPY . .

EXPOSE 3000

RUN npm install && CI=true npm test && npm run build

CMD ["npm", "start"]
```
___
## NGINX file configuration

```nginx
events { }

http {
  server {
    listen 80;
    
    location / {
      proxy_pass http://pacoder:3000;
    }
  }
}
```
___

This environment can be run with the usual
```
$ docker-compose up
```
And can be open at http://localhost