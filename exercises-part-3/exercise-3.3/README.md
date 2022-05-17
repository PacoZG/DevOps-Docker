# Implementation of exercise 3.3 - Processes as a non-root user
___
## Change on __frontend__ Dockerfile
```docker
FROM ubuntu:18.04

WORKDIR /usr/src/app

COPY . .

RUN apt-get update && apt-get install -y curl

RUN curl -sL https://deb.nodesource.com/setup_16.x | bash

RUN apt-get install -y nodejs

RUN npm install && npm run build && npm install -g serve

RUN useradd -m devuser && chown devuser /usr/src/app

USER devuser

CMD ["serve", "-s", "-l", "5000", "build"]
```
___
## Change on __backend__ Dockerfile

```docker
FROM golang:1.16

WORKDIR /usr/src/app

COPY . .

RUN go build && go test ./... 

RUN useradd -m devuser && chown devuser /usr/src/app

USER devuser

CMD ["./server"]
```
___

