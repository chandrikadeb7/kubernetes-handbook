# Labels

* Labels are key value pairs attached to pods, deployments, services
* For users to identify attributes of object
* Unique per object

## Labels with Selectors

Labels with selectors let you identify specific set of objects

* **Equality based selector**: labels equal/unequal
* **Set based selector**: labels in/not in/exists
* Used with **kubectl**

{% file src="../.gitbook/assets/helloworld-pod-with-labels.yml" %}

```text
$ kubectl create -f helloworld-pod-with-labels.yml
```

```text
$ kubectl get pods
```

```text
$ kubectl get pods - -show-labels
```

## Assigning labels to running Pods

```text
$ kubectl label po/helloworld app=myApp - -overwrite
```

{% hint style="info" %}
Overwrites the app name
{% endhint %}

```text
$ kubectl label po/helloworld author=chandrikadeb7 --overwrite
```

{% hint style="info" %}
Overwrites author name
{% endhint %}

```text
$ kubectl label po/helloworld author- 
```

{% hint style="info" %}
Deletes the label author
{% endhint %}

