# Commands used

```bash
$ docker run -it --name exer-1.4 ubuntu
```
___
```bash
$ apt-get update
```
___
```bash
$ apt-get install curl
```
___
```bash
$ sh -c 'echo "Input website:"; read website; echo "Searching.."; sleep 1; curl http://$website;'
```

```html
Input website:
helsinki.fi
Searching..
<!DOCTYPE HTML PUBLIC "-//IETF//DTD HTML 2.0//EN">
<html><head>
<title>301 Moved Permanently</title>
</head><body>
<h1>Moved Permanently</h1>
<p>The document has moved <a href="https://www.helsinki.fi/">here</a>.</p>
</body></html>
```
