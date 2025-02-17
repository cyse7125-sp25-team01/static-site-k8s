# Kubernetes Manifest Files

This repository contains Kubernetes manifest files to set up a namespace, deploy an application, and manage Docker credentials using secrets.

## Files

### `secret.yaml`

This file contains the Docker credentials required to pull images from a private Docker registry.

### `namespace.yaml`

This file creates a Kubernetes namespace named `satic-site`.

### `deployment.yaml`

This file creates a Deployment in the `static-site` namespace. The deployment uses the Docker credentials from the secret to pull the container image.

## Usage

Apply the namespace:

```bash
kubectl apply -f namespace.yaml
kubectl apply -f secret.yaml
kubectl apply -f deployment.yaml
```
