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

![emptydirYAML](https://user-images.githubusercontent.com/98219227/209424689-d6f3a3a4-75d9-4125-8c3a-4459029c676a.png)
