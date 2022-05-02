# Commands used

```bash
$ docker run -d -it --name exer-1.3 devopsdockeruh/simple-web-service:ubuntu
```

___
```bash
$ docker exec -it exer-1.3 bash
```
___
```bash
$ tail -f ./text.log
```
## result:
```
2022-04-26 10:41:55 +0000 UTC
Secret message is: 'You can find the source code here: https://github.com/docker-hy'
2022-04-26 10:41:57 +0000 UTC
2022-04-26 10:41:59 +0000 UTC
2022-04-26 10:42:01 +0000 UTC
2022-04-26 10:42:03 +0000 UTC
2022-04-26 10:42:05 +0000 UTC
...
```
