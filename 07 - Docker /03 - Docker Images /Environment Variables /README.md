* To find the environment variables set on a container that's already running,

```
docker inspect <containerID_OR_containerName>
```
Under the config section you will find the list of environment variables set on a container. 

* To know the env field from within a container, run

```
docker exec -it <containerName> env
```

