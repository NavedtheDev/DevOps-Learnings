Kubernetes provides various volume plugins that can be mounted inside the container to store some data temporarily or in a persistent manner or locally as well.


![volumes](https://user-images.githubusercontent.com/98219227/209423945-c55e7873-a074-425e-aacb-bd89cabf7ad8.png)


Have a look at this visual representation.
We will discuss each of these volume types one by one.

# Emptydir #

* This volume gets created as soon as the pod is assigned to the node. It stays throughout the lifespan of the pod and as soon as the pod is deleted, emptydir is removed. It will stay even if container crashes because it's related to pod lifecycle.
* Use Cases
       
      1. When a long computation needs to be done in memory.
      2. as a cache
      3. scratch space, for a sort algorithm for example.
* Emptydir can be either based on the node's disk attached to the node or if you specify the emptydir medium in the emptydir section, it will create a temporary filesystem and use the RAM as the volume for that.
* We can write the YAML file for that as, 
```
apiVersion: v1
kind: Pod
metadata:
  name: myvolumes-pod
spec:
  containers:
  - image: alpine
    name: myvolumes-container
    command: ['sh', '-c', 'sleep 3000']
    volumeMounts:
    - mountPath: /demo
      name: demo-volume
  volumes:
  - name: demo-volume
    emptyDir: {} 
 ```


# HostPath #

* This volume mounts a file or a directory from the node's file system into the pod. A hostpath will mount a directory which is present on the node and mount it inside the container.
* Use Cases: 

      1. Running a container that needs access to Docker internals.
      2. Deploying some node specific files through pod.
      3. It offers a powerful escape hatch for some applications.

* We do not use hostpath volume for production purposes, the reason being that suppose next time the pod gets deleted and gets recreated on a differenet node then the files that were there on the hostpath oof that node would not be on the new node. So, there will be a mismatch in the files and you will not get the desired result as expected.



# Remote Storage #
* They live outside of the kubernetes cluster.
* Unlike emptydir and hostpath volumes, in case of remote storage volumes when the pod will spin up on a new node it will mount the same remote storage volume beacause that is living outside to the cluster. In this way the data will be there even if the cluster goes down.
* Also, there won't be any inconsistencies if the pod goes from one node to the other due to eviction or any other reason.
