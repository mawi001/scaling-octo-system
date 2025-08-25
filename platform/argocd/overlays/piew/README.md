# Argo CD Overlay: piew

This directory contains the `piew` overlay for the Argo CD Helm chart.

## Features

- Enables Redis HA (`redis-ha.enabled: true`)
- Configures autoscaling for the server and repoServer components
- Sets tolerations for control-plane nodes
- Sets `server.insecure: true` for Argo CD server

## Usage

To deploy this overlay with Argo CD and Helm:

```sh
helm upgrade --install argocd argo/argo-cd -n argocd -f values.yaml
```

Make sure to adjust the command to your environment and Helm release setup.

## Directory Structure

- `values.yaml`: Overlay-specific values for the Argo CD Helm
