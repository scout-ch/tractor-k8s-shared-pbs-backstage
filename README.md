# Backstage Kubernetes Deployment

Kubernetes manifests for deploying Backstage using FluxCD and Kustomize.

## Configuration

- Uses SQLite (no PostgreSQL dependency)
- Namespace: `backstage`
- Service port: 7007

## Setup

1. Update the Backstage image reference in `kubernetes/backstage.yaml`
2. Add secrets in `kubernetes/kustomization.yaml` under `secretGenerator.literals`

## Deploy

```bash
kubectl apply -k kubernetes/
```

Or use FluxCD to manage the deployment automatically.
