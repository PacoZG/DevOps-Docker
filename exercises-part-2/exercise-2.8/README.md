# Implementation of exercise 2.8

## docker-compose file configuration

```yaml
version: '3.8'

services:
  frontend:
    image: frontend
    container_name: frontend
    build:
      context: ./example-frontend
      dockerfile: Dockerfile
  backend:
    image: backend
    container_name: backend
    build:
      context: ./example-backend
      dockerfile: Dockerfile
    environment:
      - REQUEST_ORIGIN=http://localhost
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

  postgres_db:
    image: postgres
    container_name: postgres
    restart: unless-stopped
    environment:
      - POSTGRES_HOST=postgres
      - POSTGRES_USER=postgres
      - POSTGRES_PASSWORD=postgres
      - POSTGRES_DATABASE=postgres

  nginx:
    image: nginx
    container_name: nginx
    ports:
      - 80:80
    volumes:
      - ./nginx.conf:/etc/nginx/nginx.conf
  
```
___
## nginx.conf file configuration
```nginx
events { worker_connections 1024; }

http {
  server {
    listen 80;
    
    location / {
      proxy_pass http://frontend:5000/;
    }

    location /api/ {
      proxy_pass http://backend:8080/;
    }
  }
}
```
___
## Change on *REACT_APP_BACKEND_URL* of __frontend__Dockerfile
```docker
FROM node:16

WORKDIR /usr/src/app

COPY . .

RUN npm install && npm run build && npm install -g serve

CMD ["serve", "-s", "-l", "5000", "build"]
```
___
## Change on *REQUEST_ORIGIN* of __backend__ Dockerfile

```docker
FROM golang:1.16

WORKDIR /usr/src/app

COPY . .

RUN go build && go test ./...

CMD ["./server"]
```
___
