Kubernetes Resources

K8S evolved as docker can't manage the clusers with heavy load and lack of self-healing, distirbution of requests traffic load & scaling.

Kubernetes resources are created using with YAML files. Basi Syntax is 

```
apiVersion:
kind:
metadata:
    name:

spec:

```

To apply the resource, you can run the command
```
kubectl create/apply -f <file-name>.yaml
```

To delete the resource, you can run the command
```
kubectl delete -f <file-name>.yaml
```
To delete all pods at a time
```
kubectl delete pods --all
```

To get pod details whcih are not created in default namespace
```
kubectl get pods -n <namespace-name>
```

To get pods & node details together
```
kubectl get pods ; kubectl get nodes
```

To login into specific container then
```
kubectl exec -it <metadata-name> -c <container-name> -- bash
```
Note: Number of containers created as part of single Pod then those containers can be access together and having single/same IP address

We can use alias for the frequent used commands i.e.,

```
alias ka='kubectl apply -f'
alias kd='kubectl delete -f'
alias kds='kubectl describe pod'

```