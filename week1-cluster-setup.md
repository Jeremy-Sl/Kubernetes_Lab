# 📦 Week 1: Kubernetes Cluster Setup

## 🎯 Objective
Establish a 3-node Kubernetes control plane using **K3s** on Ubuntu 24.04 in a ProxMox virtualized homelab environment. Lay the groundwork for a scalable, production-similar cluster with Git-based documentation and tooling.

---

## 🖥️ Environment

| Component       | Details                        |
|-----------------|--------------------------------|
| Host Platform   | ProxMox                        |
| Guest OS        | Ubuntu 24.04.1 LTS (Server)    |
| Node Names      | `sor-k3s-master`(.120)         |
|                 |  `sor-k3s-worker1` (.170)      |
|                 |  `sor-k3s-worker2` (.220)      |
| Access Method   | SSH enabled                    |

---

## 🔧 Tools Installed

| Tool       | Version        | Install Method                                      
|------------|----------------|-----------------------------------------------------|
| K3s        | v1.32.3+k3s1   | curl -sfL https://get.k3s.io | sh -`             
| kubectl    | v1.32.3+k3s1   | Bundled with K3s                                    
| k9s        | v0.27.4        | sudo snap install k9s                            
| Helm       | v3.17.3        | curl https://raw.githubusercontent.com/helm/helm/master/scripts/get-helm-3 | bash 

---

## 🔐 SSH Access

- SSH server installed and confirmed during OS install
- Password authentication enabled
- Verified access from host terminal using:
  ```bash
  ssh jeremy@192.168.70.220

