# Selectors

#### Selectors help to choose and find the resources that you are particularly looking for using labels.

For working with selectors, here is an example find you can proceed with. The same can be extended to deployments and services.

{% file src="../.gitbook/assets/helloworld-pod-with-labels \(1\).yml" %}

```text
$ kubectl create -f <file name for deployment>
```

```text
$ kubectl get pods - -show-labels
```

```text
$ kubectl get pods - -selector env=production
```

{% hint style="info" %}
List only the pods with environment 'production'
{% endhint %}

```text
$ kubectl get pods --selector dev-lead=carisa
```

{% hint style="info" %}
List only the pods with development lead 'Carisa'
{% endhint %}

## Working with Multiple Selectors

```text
$ kubectl get pods --selector env=production,dev-lead=carisa
```

```text
$ kubectl get pods --selector env=production,dev-lead!=carisa
```

{% hint style="info" %}
Search for multiple labels with negation. This command returns the list of pods with environment as 'production' and dev-lead not equal to 'Carisa'.
{% endhint %}

## In and Not In Operator

```text
$ kubectl get pods -l 'release-version in (1.0,2.0)' 
```

{% hint style="info" %}
in operator to get pods with specific release version range
{% endhint %}

```text
$ kubectl get pods -l 'release-version notin (1.0,2.0)'
```

{% hint style="info" %}
Example of notin operator
{% endhint %}

## Deleting pods with labels

```text
$ kubectl delete pods -l dev-lead=carisa
```

{% hint style="info" %}
Deletes all pods with a particular dev-lead 'Carisa'.
{% endhint %}

