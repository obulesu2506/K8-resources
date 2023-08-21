Namespace:

Namespace is a logical isolation of a network inside cluster. We can have different Namespaces in a cluster and can define in such a way that containers should be run in specific Namespace

Syntax:

Namespace YAML file:

```
---
apiVersion: v1cd
kind: Namesapce
metadata:
    name: <Namespace name>
...
```

Note: We can write Namespace file inside pod definition or individual file

Commands:
To check different Namespaces types in a K8s:
```
kubectl api-resources
```

To check different Namespaces types specific to Pod

```
kubectl api-resources | grep -i Pod
```

To check Namespace details in a particular cluster:

```
kubectl get ns
```

By default, Namespace can be created 4 in a cluste:
```
* default 
* kube-node-lease
* kube-public
* kube-system
```

