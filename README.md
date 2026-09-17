# Helm Chart Microservices

This project deploys the Online Boutique microservices application to Kubernetes using Helm and Helmfile.

## Project Structure

- `charts/microservice/` - reusable Helm chart for microservices
- `charts/redis/` - Redis Helm chart
- `values/` - service-specific configuration
- `helmfile.yaml` - defines all Helm releases
- `config.yaml` - Helmfile configuration
- `online-shop-microservices-kubeconfig.yaml` - Kubernetes configuration

## Deploy

Make sure the Kubernetes cluster is running and kubectl is configured.

```bash
kubectl create namespace microservices --dry-run=client -o yaml | kubectl apply -f -
helmfile sync
