# Commands used

```bash
$ docker container run -d nginx

$ docker container run -d redis

$ docker container run -d mongo
```
___
```bash
$ docker container ls
```
## result:
```
e30f14c93020   mongo     "docker-entrypoint.s…"   8 seconds ago        Up 7 seconds        27017/tcp   gallant_cerf
452c073a9d30   redis     "docker-entrypoint.s…"   58 seconds ago       Up 58 seconds       6379/tcp    dreamy_goldstine
cadaafdc9614   nginx     "/docker-entrypoint.…"   About a minute ago   Up About a minute   80/tcp      elated_noyce
```
___
```bash
$ docker container stop e3 ca
```
## result:
```
docker e3 ca
```
___
```bash
$ docker ps -a
```

## result:
```
e30f14c93020   mongo     "docker-entrypoint.s…"   50 seconds ago       Exited (0) 24 seconds ago              gallant_cerf
452c073a9d30   redis     "docker-entrypoint.s…"   About a minute ago   Up About a minute           6379/tcp   dreamy_goldstine
cadaafdc9614   nginx     "/docker-entrypoint.…"   2 minutes ago        Exited (0) 24 seconds ago              elated_noyce
```
__Terminal screeshot__
![Terminal Screenshot](./Screenshot%20terminal%20exercise%201.1.png)