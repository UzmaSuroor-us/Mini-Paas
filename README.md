# Mini PaaS (Platform as a Service) on Kubernetes 🚀

This project is a Mini Platform-as-a-Service (PaaS) built using Docker and Kubernetes.
It demonstrates how multiple applications can be deployed, managed, and exposed
through a single Kubernetes cluster using Ingress.

This project is created for learning and showcasing real-world DevOps concepts.

---

## Features

- Dockerized applications
- Kubernetes Deployments and Services
- Namespace-based isolation
- NGINX Ingress Controller
- Single ingress routing for multiple apps
- Scalable and modular design

---

## Tech Stack

- Docker
- Kubernetes
- NGINX Ingress
- YAML
- Linux
- Git & GitHub

---

## Project Structure

mini-paas/
├── app1/
│   ├── Dockerfile
│   ├── deployment.yaml
│   └── service.yaml
│
├── app2/
│   ├── Dockerfile
│   ├── deployment.yaml
│   └── service.yaml
│
├── ingress/
│   └── ingress.yaml
│
├── namespaces/
│   └── namespace.yaml
│
└── README.md

---

## Prerequisites

- Docker installed
- Kubernetes cluster (Minikube / Kind / K3s)
- kubectl configured
- Git installed

---

## Deployment Steps

### Step 1: Clone Repository

git clone https://github.com/<your-username>/mini-paas.git
cd mini-paas

---

### Step 2: Create Namespace

kubectl apply -f namespaces/namespace.yaml

---

### Step 3: Deploy Applications

kubectl apply -f app1/
kubectl apply -f app2/

---

### Step 4: Install NGINX Ingress Controller

kubectl apply -f https://raw.githubusercontent.com/kubernetes/ingress-nginx/main/deploy/static/provider/cloud/deploy.yaml

---

### Step 5: Apply Ingress

kubectl apply -f ingress/ingress.yaml

---

## Access Applications

Add the following entry to /etc/hosts:

<node-ip> myapp.local

Then access in browser:

- http://myapp.local/app1
- http://myapp.local/app2

---

## Learning Outcomes

- Understanding how a PaaS works internally
- Kubernetes networking and ingress routing
- Deploying and exposing microservices
- Real-world DevOps workflow

---

## Future Improvements

- Helm chart support
- CI/CD pipeline integration
- Monitoring with Prometheus and Grafana
- HTTPS using Cert-Manager
- Horizontal Pod Autoscaling

---

## Author

Uzma  
DevOps Engineer | Kubernetes | Cloud

---

⭐ Star this repository if you found it useful!
