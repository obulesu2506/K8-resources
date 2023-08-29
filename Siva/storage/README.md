Volumes inside K8S :
------------------------
1) emptyDir
2) hostPath

EmptyDir (Empty directory) is a volume storage hub which will store data of all the containers inside the node and then this data will be moved to outside node (i.e., ELS) using  sidecars

Mounting config maps as volumes:
--------------------------------
1) Create configmap for files for the nginx.conf
2) Mount them as volumes
3) use it for containers

Storage/Volumes outside K8S:
-----------------------------
1) Drives/ External hard disk
2) PV - Persistent Volume
3) PVC - Persistent Volume Claims

Static Provisioning:
---------------------
you create the disk --> manual
you need to have PV --> Persistent Volumes

```
Pod --> PVC --> PV --> volume disks
```
Note: When a Pod get created then specific volume can be mounted and will request extra volume from PVC which inturn request from PV--> underlying disks/drives

Life Cycle Policies:
---------------------
Retain --> Even if Pod deleted then K8S ensures the data shouldn't be lost
Delete --> if Pod deleted, your data will get deleted.
Recycle --> Disk can't be deleted but data will get deleted.

Access Modes:
--------------
RWO --> Multiple Pods, only one pod is allowed to write, remaining pods are for read
RWM --> all pods can read/write
RO  --> only for reading the data

EBS Static Provisioning:
----------------------------
If EC2 is one region, then corresponding EBS should be in that same region
