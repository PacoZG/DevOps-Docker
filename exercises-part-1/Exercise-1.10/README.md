# Commands used

```bash
$ docker build .  -t web-server  
```

```bash
$ docker run -p 3000:8080 web-server
```

## result:
```
WARNING: The requested image's platform (linux/amd64) does not match the detected host platform (linux/arm64/v8) and no specific platform was requested
[GIN-debug] [WARNING] Creating an Engine instance with the Logger and Recovery middleware already attached.

[GIN-debug] [WARNING] Running in "debug" mode. Switch to "release" mode in production.
 - using env:	export GIN_MODE=release
 - using code:	gin.SetMode(gin.ReleaseMode)

[GIN-debug] GET    /*path                    --> server.Start.func1 (3 handlers)
[GIN-debug] Listening and serving HTTP on :8080
[GIN] 2022/04/29 - 10:02:08 | 200 |       3.551ms |      172.17.0.1 | GET      "/"
[GIN] 2022/04/29 - 10:02:08 | 200 |         287µs |      172.17.0.1 | GET      "/favicon.ico"
[GIN] 2022/04/29 - 10:02:48 | 200 |         474µs |      172.17.0.1 | GET      "/"
[GIN] 2022/04/29 - 10:05:41 | 200 |         250µs |      172.17.0.1 | GET      "/"
```


Commands used on the second terminal
===
```bash
$ curl localhost:3000
```

## result:
```json
{"message":"You connected to the following path: /","path":"/"}
```