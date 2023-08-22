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

NodePort:
NodePort provide facility to the webuser to access nodes over a network using same IP for connecting different nodes(servers)

user: NODE1:<NODE-PORT> --> ClusterIP --> Container
      NODE2:<NODE-PORT> --> ClusterIP --> Container

LoadBalancer:
This is used to access different nodes via LB IP

LB --> ELB --> connecting to any of the instances --> Pod

```
ClusterIP is subset of NodePort
NodePort is subset of LoadBalancer
```