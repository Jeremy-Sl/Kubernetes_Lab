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

- [ ] Create `whoami` Deployment
- [ ] Create `whoami` Service
- [ ] Create `whoami` Ingress
- [ ] Access nginx via browser (`nginx.lab.local`)
- [ ] Access whoami via browser (`whoami.lab.local`)
- [ ] Scale nginx Deployment
- [ ] Scale whoami Deployment
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
| `kubectl-get-pods-week3.png`     | Both nginx and whoami Pods running |
| `kubectl-get-svc-week3.png`      | Services for nginx and whoami created |
| `kubectl-get-ingress-week3.png`  | Ingress rules for both apps applied |
| `browser-nginx-lab-local.png`    | Accessing nginx via browser |
| `browser-whoami-lab-local.png`   | Accessing whoami via browser |
| (Optional) `kubectl-get-deployments-scaled.png` | Verification of scaling replicas |
| (Optional) `dashboard-access.png` | Kubernetes Dashboard GUI |

---

## 📂 Deployment Manifests

**whoami-deployment.yaml**

**whoami-service.yaml**

**whoami-ingress.yaml**

**dashboard.yaml**

## 📚 Learnings and Key Concepts

(Placeholder — Summarize what you learn about deploying multiple apps, Services, Ingress, and scaling.)

## 📈 Next Steps
1. Deploy a full multi-container app (e.g., WordPress + MariaDB)

2. Implement basic security practices: limit Ingress access, secure services.

3. Introduce TLS with Traefik (Let's Encrypt certificate management).
