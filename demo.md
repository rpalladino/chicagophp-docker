# Demo

## Single Container

```bash
cd ~/Repositories/chicagophp-docker/examples/01-single

docker-machine ls

docker-machine start # if necessary

eval $(docker-machine env default)

docker version

cat Dockerfile

docker build -t rpalladino/myapp1 .

docker images

docker run -d -p 8000:8000 rpalladino/myapp1

docker ps

<check in browser>

docker logs CONTAINER # -f to follow

docker stop CONTAINER

docker ps # -a to show all including exited

docker start CONTAINER

docker run -d -p 8001:8000 rpalladino/myapp1

time docker run -d -p 8002:8000 rpalladino/myapp1

kitematic

docker exec -it CONTAINER bash
```

## Multi-container with Compose

```

```
