# Homework

## Description
This *application* is an image of my personal [website]('http://pacoder.com) that has been developt with ReactJS, Tailwind and other tools. For more information about the base code go [here](https://github.com/PacoZG/pacoder)

## The way I builed the image
- First I clone the repository in my local machine
- I created a [Dockerfile](./Dockerfile) which I used to build the image that I called __pacoder__

## Tagging the image
```bash
$ docker tag pacoder sirpacoder/pacoder
```
## Pushing the image
```bash
$ docker push sirpacoder/pacoder   
```

## How to run the application:
Run thise following script in the terminal
```bash
$ docker pull sirpacoder/pacoder:latest
```
followed by:
```bash
$ docker run -p 3000:3000 sirpacoder/pacoder
```
You can navigate the application on the http://localhost:3000