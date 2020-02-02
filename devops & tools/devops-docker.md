
## Articles & Tutorials

[Dockerize a node app](https://nodesource.com/blog/dockerizing-your-nodejs-applications)


## Running mongodb dockerized

```sh
docker run -d -p 27017:27017 --name mongodb dockerfile/mongodb mongod --smallfiles
```

## Remove images

```sh
docker images --no-trunc
docker rmi <image_id>
```

## Docker word reference

* **registry**: A collection of named repositories.
* **repository**: A collection of diferent images built from the same source.
* **image**: A container resulting of pulling from a registry or build from a Dockerfile.

[More info](http://blog.thoward37.me/articles/where-are-docker-images-stored/)

## Change docker files location

Edit `/etc/default/docker` and add:

```sh
DOCKER_OPTS="-g /path/to/docker/data"
```

<!--stackedit_data:
eyJoaXN0b3J5IjpbNDQxMjg1MjY0XX0=
-->