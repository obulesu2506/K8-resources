A ConfigMaps is an API object used to store non-confidential data in key-value pairs. 
Pods can consume ConfigMaps as environment variables, command-line arguments, or as configuration files in a volume.

Syntax:

```
apiVersion: v1
kind: ConfigMap
metadata:
    name:
```