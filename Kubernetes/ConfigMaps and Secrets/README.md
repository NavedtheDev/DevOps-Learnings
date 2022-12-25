ConfigMaps and Secrets are another set of ephemeral volumes. These can be mounted as a volume inside a container. 

# ConfigMaps #

It is used to store a set of configurations.

Here is a configmap which is mounted as a volume.
```
apiVersion: v1
kind: ConfigMap
metadata:
  name: cm-for-volume
  namespace: default
data:
  key1: val1
  key2: val2
```
```
apiVersion: v1
kind: Pod
metadata:
  name: cm-volume
  spec:
    containers:
      - name: demo
        image: busybox
        command: ["/bin/sh", "-c", "ls /home/config"]
        volumeMounts:
        - name: cm-volume
          mountPath: /home/config
    volumes:
    - name: cm-volume
      configMap:
        name: cm-for-volume
```


# Secrets #

It is used to store secret data.

Here is a secret which is mounted as a volume.
```
apiVersion: v1
kind: Secret
metadata: 
  name: demo
data:
  username: 
  password:
```
```
apiVersion: v1
kind: Pod
metadata:
  name: secret-pod-volume
  spec:
    containers:
      - name: demo2
        image: nginx
        volumeMounts:
        - name: vol-secret
          mountPath: /etc/vol-secret
    volumes:
    - name: vol-secret
      secret:
        secretName: demo
```
