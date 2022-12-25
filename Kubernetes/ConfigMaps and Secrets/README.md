ConfigMaps and Secrets are another set of ephemeral volumes. These can be mounted as a volume inside a container. 

# ConfigMaps #

It is used to store a set of configurations 



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
