# devops-with-docker - https://devopswithdocker.com/

## Part 1

### Exercise 1.1

```
CONTAINER ID   IMAGE           COMMAND                  CREATED          STATUS                     PORTS     NAMES
9598a010bf9e   nginx           "/docker-entrypoint.…"   16 seconds ago   Exited (0) 2 seconds ago             wonderful_goldwasser
505eb696f297   nginx           "/docker-entrypoint.…"   19 seconds ago   Exited (0) 2 seconds ago             quirky_dubinsky
3b9e90985f5d   nginx           "/docker-entrypoint.…"   29 seconds ago   Up 26 seconds              80/tcp    sad_shaw
```

### Exercise 1.2

```
REPOSITORY   TAG       IMAGE ID       CREATED        SIZE

CONTAINER ID   IMAGE           COMMAND                  CREATED      STATUS                  PORTS     NAMES                SIZE
```

### Exercise 1.3

```
Secret message is: 'You can find the source code here: https://github.com/docker-hy'
```

### Exercise 1.4

```
docker container run --rm -it ubuntu sh -c 'apt-get update && apt-get install -y curl; echo "Input website:"; read website; echo "Searching.."; sleep 1; curl http://$website;'
```

### Exercise 1.5

```
REPOSITORY                          TAG       IMAGE ID       CREATED        SIZE
devopsdockeruh/simple-web-service   ubuntu    4e3362e907d5   5 weeks ago    83MB
devopsdockeruh/simple-web-service   alpine    fd312adc88e0   5 weeks ago    15.7MB
```

### Exercise 1.6

```
You found the correct password. Secret message is:
"This is the secret message"

Command given to get the answer: basics
```

### Exercise 1.7

[Dockerfile](part1/1.7/Dockerfile)

```
docker run --rm -it web-server
```

### Exercise 1.8

[Dockerfile](part1/1.8/Dockerfile)

```
docker run --rm -it curler
```

### Exercise 1.9

```
docker run --rm -d -v "$(pwd)/text.log:/usr/src/app/text.log" devopsdockeruh/simple-web-service
```

### Exercise 1.10

[Dockerfile](part1/1.7/Dockerfile)

```
docker run --rm -p 8002:8080 -d web-service
```

### Exercise 1.11

[Dockerfile](part1/1.11/Dockerfile)

```
docker build . -t spring-example && docker run -p 8003:8080 spring-example
```

### Exercise 1.12

[Dockerfile](part1/1.12/Dockerfile)

```
docker build . -t example-frontend && docker run -p 5000:5000 example-frontend
```
