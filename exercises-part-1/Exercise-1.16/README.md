# Commands used

## Heroku commands

__Login__:
```bash
$ heroku login
```
__Creating app__:
```bash
$ heroku create web-zavala
```

## Docerk commands

__Image pull__:
```bash
$ docker pull devopsdockeruh/coursepage
```

__Image tag__:
```bash
$ docker tag devopsdockeruh/coursepage registry.heroku.com/web-zavala/web
```

__Images on Docker__:
```
REPOSITORY                           TAG       IMAGE ID       CREATED       SIZE
devopsdockeruh/coursepage            latest    a445883bd117   2 weeks ago   208MB
registry.heroku.com/web-zavala/web   latest    a445883bd117   2 weeks ago   208MB
````

__Push image to Docker__:
```bash
$ docker push registry.heroku.com/web-zavala/web 
````

__Heroku release__:
```bash
$ heroku container:release web --app web-zavala
```

## result:
````
Releasing images web to web-zavala... done
````

Check the result at the __[App link](https://web-zavala.herokuapp.com/)__