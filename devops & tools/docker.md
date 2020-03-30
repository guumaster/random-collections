

### Containerization

* [Docker/Node Best practices](https://github.com/nodejs/docker-node/blob/master/docs/BestPractices.md#cmd)
* [dumb-init/README.md at master · Yelp/dumb-init](https://github.com/Yelp/dumb-init/blob/master/README.md)


### Articles & Tutorials

* [Dockerize a node app](https://nodesource.com/blog/dockerizing-your-nodejs-applications)
* [More info](http://blog.thoward37.me/articles/where-are-docker-images-stored/)

### Compose show IPs of all containers

```sh
docker-compose -f /tmp/voting-app/docker-compose.yml ps -q \
  | xargs docker inspect  --format \
  '{{ range .NetworkSettings.Networks }}{{ .IPAddress }} {{ $.Name }}{{ println }}{{ end }}'
```

### Remove images

```sh
docker images --no-trunc
docker rmi <image_id>
```

### Change docker files location

Edit `/etc/default/docker` and add:

```sh
DOCKER_OPTS="-g /path/to/docker/data"
```

<!--stackedit_data:
eyJoaXN0b3J5IjpbOTY5NzQwMjY1XX0=
-->