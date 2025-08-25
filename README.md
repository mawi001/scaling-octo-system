# IoT Lab Kubernetes Platform

This repository contains the Kubernetes platform configuration for the IoT Lab, including application manifests, overlays, and infrastructure components.

## Structure

- `apps/` - Application manifests and kustomize bases/overlays (e.g., Node-RED)
- `cilium/` - Cilium CNI configuration and overlays
- `cloudflare-kubernetes-gateway/` - Cloudflare Gateway manifests and overlays
- `docs/` - Documentation and guides
- `platform/argocd/` - Argo CD Helm chart bases and overlays for GitOps
- `talos/` - Talos Linux cluster configuration and kubeconfigs

## Getting Started

1. **Install Talos Linux clusters**
   See [INSTALL.md](INSTALL.md) for Talos installation and cluster bootstrap instructions.

2. **Configure Kubernetes networking**
   Apply Cilium manifests from `cilium/`.

3. **Set up Argo CD**
   Deploy Argo CD using the Helm chart and overlays in `platform/argocd/`.

4. **Deploy applications**
   Use Argo CD to manage and deploy applications from the `apps/` directory.

## Usage

- See [platform/argocd/overlays/piew/README.md](platform/argocd/overlays/piew/README.md) for overlay-specific Argo CD deployment instructions.
- Refer to [INSTALL.md](INSTALL.md) for cluster setup and operational notes.

## Documentation

- Platform and operational docs are in the `docs/` directory.
