
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
Deployments:
---------------
Advantages:
1) Maintaining history of Deployments
2) We have feasibility to rollback/revert the version if there are any issues immediately
3) Check the deployment status
4) Rolling updates i.e., slowly implementing the new changes in the production environment and removing old version
out of 10 replicas, one by one container get recreated with new version automatically in seconds

Disadvantages:
1) Everytime need to delete the Pod and recreate the with newer version

Daemonset:
-----------
This is ensures that atleast one Pod should run on each node

