This folder consists of all Pod manifest/definition files for different purpose

1) Basic nginx (software) creation 
2) Multi containers i.e., one is software and another one is OS
3) imagePullPolicy i.e., always pull the mentioned specified source from Dockerhub before creating container instead from K8S repository
Note: There might be chances updating partially by someone/us aby don't update local repository
4) requests (Soft Limit) & limits (Hard Limit): This will ensures that specific container should run defined range and alert to cluster when reaches to maximum threshold. If crossed the limits then Pod get restarted and may not give good performance.
Note: If Pod definition file failed to provide/defined this resources(requests/limits) attributes, admin people will control using "LimitRange" while defining clusters

```
apiVersion: v1
kind: LimitRange
metadata:
    name: <filename>

```
5) Define LimitRange
6) K8S do healthchecks using "Liveness probe" and " Readiness probe" inorder to restart container if there is chance of overload

liveness probe --> When containers starts running
readiness probe --> whether the container is ready to server requests or not

Note: If we want to see the logs of the container creation and logs then give below command

```
watch kubectl get pods
```
7) If we mention image version which is not mentioned in the docker hub then K8S will create POD with "ErrImagePull" status.
   If we define two images i.e., one is valid image and another one with valid image but not mentioning any ports then, 
   status of one container is running and another one is "CrashLoopRange" error will get.

8) 

