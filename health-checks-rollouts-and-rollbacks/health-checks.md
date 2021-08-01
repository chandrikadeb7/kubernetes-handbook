# Health Checks

#### Health of a pod can be found out from it's pod events, which may prevent the pod to start running.

Some common health issues of pods are as follows.

* Container port and http get port should be same.
* Liveliness or readiness probe failed status can be checked.

## Checking pod status

```text
$ kubectl describe po/<pod-name>
```

{% hint style="info" %}
Gives the pod status events unhealthy.
{% endhint %}

