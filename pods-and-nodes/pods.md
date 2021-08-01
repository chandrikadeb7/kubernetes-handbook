# Pods

### **Pod is the smallest unit of deployment to interact with in a K8s cluster.**

* Can be created/deleted/deployed
* Represents one running process on your cluster

## A pod contains:

* Docker application container
* Storage resources
* Unique IP
* Options to govern how containers should run

## Features of a pod

* Multiple Docker containers can run in a pod
* Pod represents one single unit, a single instance of the application in K8s
* It is tightly coupled and shares resources.
* Ephemeral, disposable
* Never self starts \(by scheduler\) or self heals
* Higher level constructs to add pod stability called controllers

## **Pod States**

1. **Pending** - accepted by K8s system, but container creation is pending
2. **Running** - scheduled on a node and all of its containers are created, with at least one in running state
3. **Succeeded** - all containers in the pod have exited with exit status 0 \(successful execution, will not be restarted\)
4. **Failed** -  all containers in the pod have exited with exit status 0, but one failed with non-zero status
5. **CrashLoopBackOff** - container fails to start for some reason and K8s tries over n over again to restart

