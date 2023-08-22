Service:

Usually AWS & K8S will generate ephermal ports i.e., can't gaurantee that will get static IP if any Host restarted.

So, Service is an abstraction which defines a logical set of Pod and a policy by which to access them i.e., which will helps toexpose the pods over a network.
Each service object defines logical set of endpoints(Pods) along with a policy about how to make those Pods accessible

Three Different Types of services:
1) Node Port  - 
2) Load Balancer - distributing traffic to different nodes
3) Cluster IP  - Communicate between Pod to Pod

To get number of services in a cluster:

```
kubectl get svc
```
