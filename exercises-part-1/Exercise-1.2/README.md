# Commands used

```bash
$ docker container ls
```
## result:
```
e30f14c93020   mongo     "docker-entrypoint.s…"   32 minutes ago   Exited (0) 32 minutes ago              gallant_cerf
452c073a9d30   redis     "docker-entrypoint.s…"   33 minutes ago   Up 33 minutes               6379/tcp   dreamy_goldstine
cadaafdc9614   nginx     "/docker-entrypoint.…"   34 minutes ago   Exited (0) 32 minutes ago              elated_noyce
```
___
```bash
$ docker image ls
```
## result:
```
mongo        latest    f7ee9200a31b   4 days ago   665MB
redis        latest    cf8e017ea3f3   5 days ago   107MB
nginx        latest    d17025d71df5   5 days ago   134MB
```
___
```bash
$ docker container stop 45
```
## result:
```
docker 45
```
___
```bash
$ docker container rm e3 45 ca
```

## result:
```
docker e3 45 ca
```
___
```bash
$ docker image rm mongo redis nginx
```

__Terminal screeshot__
![Terminal Screenshot](./Screenshot%20terminal%20exercise%201.2.png)