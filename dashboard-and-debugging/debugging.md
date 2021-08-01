# Debugging

## Pod Monitoring and Logging

Describe deployments or pods for obtaining the subsequent events.

```
$ kubectl describe po/<pod-name>
```

{% hint style="warning" %}
Replace &lt;pod-name&gt; with the name of your pod.
{% endhint %}

Get the pod logs using the below command.

```text
$ kubectl logs <pod-name>
```

## Exec into the pod

```text
$ kubectl exec -it <pod-name> /bin/bash
```

```text
$ ps -ef
```

{% hint style="info" %}
See all processes inside the pod using this command.
{% endhint %}

```text
$ exit
```

{% hint style="info" %}
Type exit command to come out of the pod.
{% endhint %}



## Thanks for reading. Hope you're having a good day! 

