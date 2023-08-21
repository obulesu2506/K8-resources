Namespace:

Namespace is a logical isolation of a network inside cluster. We can have different Namespaces in a cluster and can define in such a way that containers should be run in specific Namespace

Syntax:

Namespace YAML file:

```
apiVersion: v1
kind: Namesapce
metadata:
    name: <Namespace name>
```