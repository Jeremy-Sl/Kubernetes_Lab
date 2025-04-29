# 📦 Week 2: Application Deployment and Routing

---

## 🎯 Objective

Deploy a sample web application (nginx) on the Kubernetes cluster.  
Expose the application externally using the Traefik Ingress Controller pre-installed with K3s.

---

## 🛠 Environment

| Component               | Details |
|--------------------------|---------|
| Kubernetes Distribution  | K3s |
| Nodes                    | 1 control-plane, 2 worker nodes |
| Ingress Controller       | Traefik (bundled with K3s) |
| OS Platform              | Ubuntu 24.04.2 LTS |
| Tools                    | kubectl |

---

## 📋 Tasks Completed

- [x] Create nginx Deployment
- [x] Create ClusterIP Service
- [x] Create Ingress Resource
- [x] Verify External Access
- [x] Document Configurations and Outputs

---

## 🔧 Tools Used

- kubectl
- Traefik (already installed with K3s)

---

## 📸 Outputs and Screenshots

| Screenshot/File Name | Description |
|----------------------|-------------|
| `kubectl-get-deployments.png` | (Placeholder) |
| `kubectl-get-services.png`    | (Placeholder) |
| `kubectl-get-ingress.png`     | (Placeholder) |
| `browser-nginx.png`           | (Placeholder) |

---

## 📂 Deployment Manifests

**nginx-deployment.yaml**
Wrote and applied the YAML file to deploy two nginx pods in the cluster using a Deployment resource.  
*(file in /manifests)*

**nginx-service.yaml**
Wrote and applied the YAML file to create a ClusterIP Service that provides internal access and load balances traffic across the nginx pods.  
*(file in /manifests)*

**nginx-ingress.yaml**
Wrote and applied the YAML file to define an Ingress rule that exposes the nginx Service externally through the Traefik Ingress Controller.  
*(file in /manifests)*
