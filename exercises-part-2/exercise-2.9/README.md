# Implementation of exercise 2.8

## docker-compose file configuration
For this exercise I use the docker compose file from exercise 2.6 on which we didn't integrate NGINX and the buttons worked properly.

```yaml
version: '3.8'

services:
  frontend:
    image: frontend
    container_name: frontend
    build:
      context: ./example-frontend
      dockerfile: Dockerfile
    ports:
      - 5000:5000

  backend: 
    image: backend
    container_name: backend
    build: 
      context: ./example-backend
      dockerfile: Dockerfile
    ports:
      - 8080:8080
    environment:
      - REDIS_HOST=redis
      - POSTGRES_HOST=postgres
      - POSTGRES_USER=postgres
      - POSTGRES_PASSWORD=postgres
      - POSTGRES_DATABASE=postgres
  
  redis:
    image: redis
    container_name: redis
    restart: unless-stopped
    command: redis-server
    volumes:
      - ./redis:/data

  postgres:
    image: postgres
    container_name: postgres
    restart: unless-stopped
    environment:
      - POSTGRES_HOST=postgres
      - POSTGRES_USER=postgres
      - POSTGRES_PASSWORD=postgres
      - POSTGRES_DATABASE=postgres
    volumes:
      - ./database:/var/lib/postgresql/data
```
___
## Change on *REACT_APP_BACKEND_URL* of __frontend__ Dockerfile
```docker
FROM node:16

WORKDIR /usr/src/app

COPY . .

ENV REACT_APP_BACKEND_URL http://localhost:5000

EXPOSE 5000

RUN npm install && npm run build && npm install -g serve

CMD ["serve", "-s", "-l", "5000", "build"]
```
___
## Change on *REQUEST_ORIGIN* of __backend__ Dockerfile

```docker
FROM golang:1.16

WORKDIR /usr/src/app

EXPOSE 8080

ENV PORT 8080

ENV REQUEST_ORIGIN http://localhost:8080

COPY . .

RUN go build && go test ./...

CMD ["./server"]
```
___

