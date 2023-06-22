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

