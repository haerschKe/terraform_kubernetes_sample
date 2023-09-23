# Demo on how to run a Kubernetes App via Terraform
Deploy a simple NGINX app on Kubernetes (e.g. on Minikube) via Terraform.

## Prerequisites
- Terraform
- Minikube

## How to run
**providers.tf** contains details about the provider module (here hashicorps kubernetes) and declares the kubernetes params.

**k8s.tf** is the main file, in which we declare all the relevant Kubernetes stuff like Namespace, Deployment, etc. to run the sample NGINX app.

Commands:
````
minikube start

terraform init

terraform plan

terraform apply

kubectl get ns

kubectl get ns k8s-ns-by-tf

kubectl get deployment -n k8s-ns-by-tf

kubectl get pods -n k8s-ns-by-tf

terraform destroy

minikube stop
````
