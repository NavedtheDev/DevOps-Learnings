* By default, the docker run command pulls the latest image of the application and runs it. But what if we want to run a specific image instead of the latest one. Use the command,

```
docker run <image_name>:<tag>
```
Example,
```
docker run redis:5.0.5
```

* To run a container in an interactive mode witha terminal,

```
docker run -it <image_name>
```

* To do port mapping,

```
docker run -p <host's_port>:<container's_port>
```

* To make your data persistent,

```
docker run -v <external_directory>:<container's_directory> <container_name>
```
Example,
```
docker run -v /opt/datadir:/var/lib/mysql mysql
```

* To get information about a speciifc conatiner,

```
docker inspect <container_ID_OR_container_name>
```

* To get logs of a speciifc container,

```
docker logs <container_ID_OR_container_name>
```
