# NGINX Deployment on Kubernetes

This project demonstrates how to deploy an NGINX application on a Kubernetes cluster and access it using either `kubectl port-forward` or a LoadBalancer Service.

## Prerequisites

- Kubernetes cluster (e.g., AWS EKS, GCP GKE, Azure AKS, or Minikube)
- `kubectl` configured to interact with your cluster
- GitHub Codespaces environment (optional)

## Deployment Steps

1. **Clone the Repository**

   ```bash
   git clone https://github.com/<your-username>/<your-repo>.git
   cd <your-repo>

kubectl apply -f manifests/nginx-deployment.yaml
kubectl apply -f manifests/nginx-service.yaml

kubectl port-forward service/nginx-service 8080:80
Look for the EXTERNAL-IP in the output.

Access Application

Open your browser and navigate to http://<EXTERNAL-IP>.

Replace <EXTERNAL-IP> with the actual external IP address obtained in the previous step

kubectl delete -f manifests/nginx-deployment.yaml
kubectl delete -f manifests/nginx-service.yaml

