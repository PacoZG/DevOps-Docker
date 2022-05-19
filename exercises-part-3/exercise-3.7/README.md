# Implementation of exercise 3.7 - Image size improvement of a personal project with Alpine
- The repository/project used for this exercise can be found at [pacoder](https://github.com/PacoZG/pacoder), we only need to copy the docker-compose, dockerfile and the nginx files to the root of the project and proceed with the steps below.

## Dockerfile
```docker
# module install
FROM node:16-alpine as install-stage
WORKDIR /app

ENV PATH /app/node_modules/.bin:$PATH

COPY package.json /app/package.json

RUN npm install


# build
FROM node:16-alpine as build-stage

COPY --from=install-stage /app/node_modules/ /app/node_modules

WORKDIR /app

COPY . .

RUN npm run build


# server
FROM node:16-alpine

COPY --from=build-stage /app/build/ /app/build

RUN npm install -g serve


# start app
CMD [ "serve", "-s", "/app/build", "-l", "3000" ]
```

### The size of such image was improved from ~1.2GB to ~128MB

## I also managed to redce NGINX image by using the following configuration in the docker-compose.yml file

```yml
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
    image: nginx:1.20-alpine
    container_name: nginx
    ports:
      - 80:80
    volumes:
      - ./nginx.conf:/etc/nginx/nginx.conf
```

### The size of such image was improved from ~128 to ~25MB