# Master Node

### Master Node is responsible for overall management of cube cluster

{% file src="../.gitbook/assets/architecture.png" caption="kubenetes-architecture.png" %}

## The Master Node contains 

* **API Sever** - frontend of Kube control pane, interacts with the Kube API 
* **Scheduler** - watches created pods and designs to run on a specific node
* **Controller Manager** - controllers that runs tasks on a cluster

## There are four types of Controllers in Kubernetes

1. **Node Controller**: responsible for worker states
2. **Replication Controller**: maintains correct no. of pods for replicated controllers
3. **End-Point Controller**: joins services and pods together
4. **Service account/ Token Controller**: access mgmt.



