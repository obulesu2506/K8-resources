
Pod:
Now I want multiple replicas/pods?
Everytime I need to delete the old pod and recreate pod

Replica Set:
It can create multiple pods. Replica set gaurentee always a desired no of pods are running.
nginx-dhrh4
```
podname = [replicaset-name]-[random-name]
```
Problem: when there is a new version of application, you need to manually remove the replicaset and create again but where as in case of deployment not required using replace or scaling option
10
Deployment
10
nginx-deployment-7fb96c846b-87fb6
```
podname-[deployment_name]-[replicaset]-[random-name]
```

Pod is a subset of replicaset
replicaset is a subset of deployment

```
kubectl replace -f <manifest.yaml>
or
kubectl scale --replicas=4 -f <manifest.yaml>

```
