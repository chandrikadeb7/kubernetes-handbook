# How to Run Jobs

* Jobs run once and stop
* Cron jobs run periodically

## Listing Jobs

```text
$ kubectl get jobs
```

```text
$ kubectl get cronjob
```

## Delete/Edit Cron Job

```text
$ kubectl edit cronjob/<name> 
```

{% hint style="warning" %}
Set suspend status 'true
{% endhint %}

