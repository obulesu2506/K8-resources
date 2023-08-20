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