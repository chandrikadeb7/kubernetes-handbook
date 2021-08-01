# Nodes

### Master is responsible for managing the cluster activities and communication with nodes.

## A Node is a worker machine.

#### A node can be a virtual machine or physical machine

Following are the specific Node Requirements:

1. A Kubelet running
2. Container tool like Docker
3. Kube-proxy process running
4. Supervisord \(restart components\)

#### **Recommended: K8s in production then have at least a** **3 node cluster**

## **Kubelet**

* Communicates with API server to check if pods have been assigned to the nodes
* Execute pod containers via container engine
* Mounts and runs pod volumes and secrets
* Executes health checks for pod/node status
* Podspec : yaml file describing a pod
* Kube apiserver -&gt; podspec -&gt; kubelet -&gt; pods mentioned are running and healthy

## **Kube-proxy**

* Network proxy
* Runs on all worker nodes
* Modes:
  * User space
  * IPTables
  * IPvs \(alpha feature\)
* Watches API server for add/del of services

