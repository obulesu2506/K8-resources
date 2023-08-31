We can restrict to run the Pods on specific Nodes using below methods

1) nodeSelector:
2) Affinity & Anti-Affinity
3) nodeName
4) Pod topology

As a first step need to label the node which we selected to be executed with specified Pod

```
kubectl label node <node-name> <key>=<value>
```

To find the number of labels
```
kubectl get nodes --show-labels
```

Note: Reference for this syntax 
```
https://kubernetes.io/docs/tasks/configure-pod-container/assign-pods-nodes/#add-a-label-to-a-node
```

--> There might be chances label can be changed so need to define properly with extra conditions in POD file using below methods
i) requiredDuringSchedulingIgnoredDuringExecution
ii) preferredDuringSchedulingIgnoredDuringExecution

requiredDuringSchedulingIgnoredDuringExecution:
1) Scheduler will schedule based on labels -- hard rule
2) Before Pod execution, some may labels get changed or not.

preferredDuringSchedulingIgnoredDuringExecution:
1) Scheduler will schedule based on labels -- soft rule
2) Before Pod execution, some may labels get changed or not.

Note: If multiple labels nodes are present then based on weight preference, can get nodes

Pod Affinity:
-------------
If multiple Pods are running on the same node then latency may get affected. We can use this Pod Affinity then there might be chances to Pods will run smoothly

Taint & Tolerations:
--------------------
Taint is nothing but defining such a way that no POD shouldn't run the selected node
```
kubectl taint nodes <node-name> key1=value1:NoSchedule
```

To remove taint i.e., untainted the node
```
kubectl taint nodes <node-name> key1=value1:NoSchedule-
```

Tolerations are applied to PODs . Tolerations allow the scheduler to schedule Pods with matching taints but don't guarantee

```
tolerations:
- key: "key1"
  operator: "In"
  value: "value1"
  effect: "NoSchedule"
```



