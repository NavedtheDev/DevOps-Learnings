*  To pull an image from docker hub,

```
docker pull <image_name>
```

* To start a container from an image,

```
docker run <image_name>
```
This command is also used to pull the image from docker hub and run the the container from that image.

* To list all running conatiners,

```
docker ps
```

* To stop all the containers at once,

```
docker stop $(docker ps -aq)
```

* To remove all the stopped containers at once,

```
docker rm $(docker ps -aq)
```

* command to delete all the available images

```
docker rmi $(docker images -aq)
```
