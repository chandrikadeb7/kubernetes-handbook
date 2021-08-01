# Namespaces

## Why Namespaces?

* Multiple virtual clusters backed by same physical cluster
* For teams with accountability
* Divides cluster resources
* Unique names of deployments/pods

## Working with Namespaces

To get the existing namespaces in the cluster.

```text
$ kubectl get namespaces
```

To create namespace

```text
$ kubectl create namespace <name>
```

To delete a namespace

```text
$ kubectl delete namespace <name>
```

#### To deploy a resource to a specific namespace append - n &lt;namespace-name&gt;

