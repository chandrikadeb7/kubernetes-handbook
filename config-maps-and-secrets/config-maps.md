# Config Maps

Config Maps are used to change something such as URL or name at deployment time.

## Working with Config Maps

```text
$ kubectl create configmap logger - —from-literal=log_level=debug
```

{% hint style="info" %}
Create a config map with log\_level = debug
{% endhint %}

```text
$ kubectl get configmaps
```

{% hint style="info" %}
Get all config maps present in cluster
{% endhint %}

```text
$ kubectl get configmap/logger -o yaml
```

{% hint style="info" %}
Output config map as a yaml file.
{% endhint %}

