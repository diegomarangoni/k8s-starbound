# Starbound Kubernetes Dedicated Server

This repository contains resources for running a [Starbound](https://playstarbound.com/) server.

*Tested in GKE 1.12*

## Using

Git clone this repository

```
git clone https://github.com/diegomarangoni/k8s-starbound.git

cd k8s-starbound/
```

Replace the steam credentials secret file [steam.yml](steam.yml) with valid credentials (base64 encoded) and apply with:

```
kubectl apply -f steam.yml
```

Now, apply the entire [starbound](starbound/) folder with:

```
kubectl apply -f starbound/
```

Get your server public IP address with the following command:

```
kubectl get services
```
