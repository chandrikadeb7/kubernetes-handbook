# Worker Nodes

{% file src="../.gitbook/assets/architecture.png" caption="Kubernetes-architecture.png" %}

## Functions

* Worker nodes is the location where your apps operate
* Communication between master and worker nodes is via **kubelet** process
* Docker along with kubelet works together on worker nodes to run containers on node

## Kube-proxy

* Network proxy/load balancer on single worker node
* Handles network routing for TCP/UDP packets
* Connection forwarding

## Pod

* Pod is smallest unit of deployment in Kubernetes
* Containers in a pod are tightly coupled and share storage, linux namespaces, IP addresses etc.

## Post Scheduling

* Once pods are scheduled and running 
  * kubelet process checks health
  * Kube-proxy routes packets from communicating processes
* Worker nodes are exposed to the internet and traffic coming in is handled via kube-proxy
* User thus communicates with the Kube app

