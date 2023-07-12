*  To pull an image from docker hub,

```
docker pull <image_name>
```

* To start a container from an image,

```
docker run <image_name>
```
This command is also used to pull the image from docker hub and run the the container from that image.

* To run a command in a detached mode,

```
docker run -d <image_name>
```

* To list all running containers,

```
docker ps
```

* To see all the running as well as stopped containers,

```
docker ps -a 
```

* To stop a single container,

```
docker stop <container_ID>
```

* To remove a single container,

```
docker rm <container_ID>
```

* To stop all the containers at once,

```
docker stop $(docker ps -aq)
```

* To remove all the stopped containers at once,

```
docker rm $(docker ps -aq)
```

* To delete a single image,

```
docker rmi <image_name>
```

* To delete all the images,

```
docker rmi $(docker images -aq)
```

* To restart a container afer stopping it,

```
docker start <container_ID_of_stopped_container>
```
