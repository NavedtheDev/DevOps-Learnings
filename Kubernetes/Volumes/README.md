Kubernetes provides various volume plugins that can be mounted inside the container to store some data temporarily or in a persistent manner or locally as well.


![volumes](https://user-images.githubusercontent.com/98219227/209423945-c55e7873-a074-425e-aacb-bd89cabf7ad8.png)


Have a look at this visual representation.
We will discuss each of these volume types one by one.

# Emptydir #

* This volume gets created as soon as the pod is assigned to the node. It stays throughout the lifespan of the pod and as soon as the pod is deleted, emptydir is removed. It will stay even if container crashes because it's related to pod lifecycle.
