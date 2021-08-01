# Secrets

Secrets are useful for encrypting user credentials inside your pods or services.

## Working with Secrets

**Creating a secret**

```text
$ kubectl create secret generic apikey —from-literal=api_key=186289106
```

**List all secrets**

```text
$ kubectl get secrets
```

**Ouput the secret as a yaml file**

```text
$ kubectl get secret apikey -o yaml
```

