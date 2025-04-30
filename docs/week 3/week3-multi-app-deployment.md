# 📦 Week 3: Multi-App Deployment, Routing, and Scaling

---

## 🎯 Objective

Deploy multiple applications on the Kubernetes cluster, expose them externally using Ingress rules, and perform basic manual scaling to simulate real-world application management.

---

## 🛠 Environment

| Component               | Details                         |
|--------------------------|---------------------------------|
| Kubernetes Distribution  | K3s v1.32.3+k3s1                |
| Nodes                    | 1 control-plane, 2 worker nodes |
| Ingress Controller       | Traefik (bundled with K3s)      |
| OS Platform              | Ubuntu 24.04.2 LTS              |
| Tools                    | kubectl, nano, (Optional: Helm) |

---

## 📝 Plan for Week 3

- Deploy a second simple application (`whoami`) alongside nginx.
- Create ClusterIP Services for both applications.
- Define separate Ingress routes for each app:
  - `nginx.lab.local`
  - `whoami.lab.local`
- Verify external browser access for both apps.
- Perform manual scaling:
  - Increase and decrease the number of nginx Pods.
  - Increase and decrease the number of whoami Pods.
- (Optional Bonus) Deploy and access the Kubernetes Dashboard.

---

## 📋 Tasks Completed

- [x] Create `whoami` Deployment
- [x] Create `whoami` Service
- [x] Create `whoami` Ingress
- [x] Access whoami via browser (`whoami.lab.local`)
- [x] Scale nginx Deployment
- [x] Scale whoami Deployment
- [ ] (Optional) Deploy Kubernetes Dashboard
- [ ] Document outputs and screenshots

---

## 🔧 Tools Used

- kubectl
- Traefik (pre-installed with K3s)
- nano
- (Optional) Kubernetes Dashboard
- (Optional) Helm

---

## 📸 Outputs and Screenshots

| Screenshot/File Name            | Description                       |
|----------------------------------|-----------------------------------|
| `kubectl get pods - whoami.png`     | Both nginx and whoami Pods running |
| `kubectl get service - whoami.png`      | Services for nginx and whoami created |
| `kubectl get ingress - whoami.png`  | Ingress rules for both apps applied |
| `whoami online.png`   | Accessing whoami via browser |
|  `kubectl scale deployments nginx.png` | Verification of scaling nginx |
|  `kubectl scale deployments whoami.png` | Verification of scaling whoami |
| (Optional) `dashboard-access.png` | Kubernetes Dashboard GUI |

---

## 📂 Deployment Manifests

**whoami-deployment.yaml**
Wrote and applied the YAML file to deploy one whoami pod in the cluster using a Deployment resource.  
*(file in /manifests)*

**whoami-service.yaml**
Wrote and applied the YAML file to create a ClusterIP Service that provides internal access.
*(file in /manifests)*

**whoami-ingress.yaml**
Wrote and applied the YAML file to define an Ingress rule that exposes the whoami Service externally through the Traefik Ingress Controller.  
*(file in /manifests)*

**dashboard.yaml**

## 📚 Learnings and Key Concepts

(Placeholder — Summarize what you learn about deploying multiple apps, Services, Ingress, and scaling.)

## 📈 Next Steps
1. Deploy a full multi-container app (e.g., WordPress + MariaDB)

2. Implement basic security practices: limit Ingress access, secure services.

3. Introduce TLS with Traefik (Let's Encrypt certificate management).
