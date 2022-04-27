# Commands used

```bash
$ docker run -it devopsdockeruh/pull_exercise
```


Commands used on the second terminal
===
```bash
$ docker container ls -a
```

## result:
```
CONTAINER ID   IMAGE                          COMMAND           CREATED              STATUS              PORTS     NAMES
8d11aced2edb   devopsdockeruh/pull_exercise   "node index.js"   About a minute ago   Up About a minute             competent_banach
```


```bash
$ docker exec -it competent_banach sh
```
```
/usr/app # ls
Dockerfile  README.md   index.js
/usr/app # cat README.md
This is the readme, use input "basics" to complete this exercise.
/usr/app # exit
```