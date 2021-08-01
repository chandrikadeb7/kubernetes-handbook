# Running Hello World Application

## Hello World Deployment in Kubernetes

Open Docker Desktop and run **Docker**.

Open **Terminal** to start **Minikube**.

```
$ minikube start
```

```bash
$ kubectl get all
```

{% hint style="info" %}
 Lists all the resources present in the cluster, i.e. pods, services, deployments, replicas. 
{% endhint %}

{% file src="../.gitbook/assets/helloworld.yaml" %}

Use this deployment file for Hello World application.

```bash
$ kubectl create -f helloworld.yaml
```

Expose the deployment as Node port to view in browser.

```bash
$ kubectl expose deployment helloworld --type=NodePort
```

Open your deployment in a browser!!

```bash
$ minikube service helloworld
```

