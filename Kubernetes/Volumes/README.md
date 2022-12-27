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
```
apiVersion: v1
kind: Pod
metadata: 
  name: pod-using-nfs
spec: 
  volumes:
    - name: nfs-volume
      nfs: 
        server: 91.211.152.190
        path: /var/nfsshare
  containers:
    - name: app
      image: alpine
      volumeMounts:
        - name: nfs-volume
          mountPath: /mnt
      command: ["/bin/sh"]
      args: ["-c", "while true; do date >> /mnt/dates.txt; sleep 5; done"]
```



# Persistent Volume and Persistent Volume Claim #

* Persistent volume claim is a kubernetes object. Whenever a PVC is created the master control loop will look for the new PVCs and will try to find the corresponding PV and try to bind it to that.
* Now what a PV is ? PV stands for persistent volume. It is the actual storage basically the abstraction of the actual storage backend, and it is also a kubernetes object. It defines the storage inside the cluster. It's also the abstraction which is linked to the external storage.
* Persistent volume has to be created by the admin. It can be created statically or dynamically. If a storage class is present then it is a dynamic provisioning else it's a static provisioning. 
* Suppose you create a PVC and there is no storage class, so the PVC will remain unbound. Now you create a PV manually, and once the PV is created manually, then the PVC gets bound to that PV. So this was an example of static provisioning.
* In case of dynamic provisioning, we need to define a storage class. In Kubernetes there are differenet types of storage class that can be used and have different sets of configurations. Now when the user creates the PVC, the PV gets automatically created. There are a lot of benefits to it. 
* Now what is a storage class ? Storage class defines what kind of storage will be provisioned when a PVC is created dynamically.
```
apiVersion: storage.k8s.io/v1
kind: StorageClass
metadata:
 name: local-storage
provisioner: kubernetes.io/no-provisioner
volumeBindingMode: WaitForFirstConsumer
 ```
 ```
apiVersion: v1
kind: PersistentVolume
metadata:
  name: demo-pv
  labels:
    type: local
spec:
  storageClassName: local-storage
  capacity:
    storage: 5Gi
  accessModes:
    - ReadWriteOnce
  hostPath: 
    path: "/opt/data"
```
```
apiVersion: v1
kind: PersistentVolumeClaim
metadata:
  name: demo-pvclaim
spec:
  storageClassName: local-storage
  accessModes:
    - ReadWriteOnce
  resources:
    requests:
      storage: 3Gi
```
```
apiVersion: v1
kind: Pod
metadata:
  name: task-pv-pod
spec:
  volumes:
    - name: pv-vol
      persistentVolumeClaim:
        claimName: demo-pvclaim
  containers:
    - name: pv-pod
      image: nginx
      ports:
        - containerPort: 80
          name: "http-server"
      volumeMounts:
        - mountPath: "/usr/share/nginx/html"
          name: pv-vol
```


## How to create a PersistentVolume and PersistentVolumeClaim ##
```
apiVersion: v1
kind: PersistentVolume
metadata:
 name: demo-pv
 labels:
   type: local
spec:
 storageClassName: manual
 capacity:
   storage: 5Gi
 accessModes:
   - ReadWriteOnce
 hostPath: 
   path: "/mnt/data"
   ```
   
