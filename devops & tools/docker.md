
## Articles & Tutorials

* [Dockerize a node app](https://nodesource.com/blog/dockerizing-your-nodejs-applications)
* [More info](http://blog.thoward37.me/articles/where-are-docker-images-stored/)



## Remove images

```sh
docker images --no-trunc
docker rmi <image_id>
```
## Change docker files location

Edit `/etc/default/docker` and add:

```sh
DOCKER_OPTS="-g /path/to/docker/data"
```

<!--stackedit_data:
eyJoaXN0b3J5IjpbLTQzOTU4MTAzXX0=
-->