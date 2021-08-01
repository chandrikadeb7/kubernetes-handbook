# Rollouts and Rollbacks

**Upgradation or rollback** to a particular version is possible with running deployments.

Use this example file to understand the commands associated with rollouts and rollbacks. 

{% file src="../.gitbook/assets/helloworld-black.yaml" %}

## Rollouts

```text
$ kubectl create -f helloworld-black.yaml --record==true
```

```text
$ minikube service navbar-service
```

```text
$ kubectl set image deployment/navbar-deployment helloworld=karthequian/helloworld:blue
```

{% hint style="info" %}
Set an updated docker image for rollout
{% endhint %}

```text
$ kubectl rollout history deployments/navbar-deployment 
```

{% hint style="info" %}
Check the rollouts image change/version history
{% endhint %}

## Rollbacks

```text
$ kubectl rollout undo deployment/navbar-deployment
```

```text
$ kubectl rollout undo deployment/navbar-deployment —to-revision=<number>
```

{% hint style="info" %}
Rollback to a particular revision.
{% endhint %}

