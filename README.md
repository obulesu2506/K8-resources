Kubernetes Resources

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

To login into container then
```
kubectl exec -it <metadata-name> -c <container-name> -- bash
```
Note: Number of containers created as part of single Pod then those containers can be access together and having single/same IP address