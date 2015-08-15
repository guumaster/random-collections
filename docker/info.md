## Running mongodb dockerized

```sh
docker run -d -p 27017:27017 --name mongodb dockerfile/mongodb mongod --smallfiles
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

