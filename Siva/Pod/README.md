This folder consists of all Pod manifest/definition files for different purpose

1) Basic nginx (software) creation 
2) Multi containers i.e., one is software and another one is OS
3) imagePullPolicy i.e., always pull the mentioned specified source from Dockerhub before creating container instead from K8S repository
Note: There might be chances updating partially by someone/us aby don't update local repository
4) requests (Soft Limit) & limits (Hard Limit): This will ensures that specific container should run defined range and alert to cluster when reaches to maximum threshold. If crossed the limits then Pod get restarted and may not give good performance.
Note: If Pod definition file failed to provide/defined this resources(requests/limits) attributes, admin people will control using "LimitRange" while defining clusters

```
apiVersion: v1
kind: Pod
metadata:
    name: imageLimitRange

```