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
  name: test-pod
  spec:
    containers:
      - name: test-pod
        image: redis
        volumeMounts:
        - name: newsecret
          mountPath: “/etc/newsecret”
          readOnly: true
    volumes:
    - name: newsecret
      secret:
        secretName: newsecret
```
