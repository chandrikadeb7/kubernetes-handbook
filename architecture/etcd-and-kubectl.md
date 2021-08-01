# etcd and kubectl

{% file src="../.gitbook/assets/architecture.png" caption="Kubernetes-architecture.png" %}

## **etcd**

* Distributed key value store
* Kubernetes uses this as its database and stores cluster data here
* Job scheduling, pod info etc.

## **kubectl**

* CLI for Kubernetes to interact with master node
* Contains kubeconfig file which has server info/ auth info to access API server

