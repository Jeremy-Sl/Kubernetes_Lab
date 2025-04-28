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
  ``ssh jeremy@192.168.70.220``

## 🖥️ Clustering

  -Joined node2 and node3 to node1 (master) with:
``curl -sfL https://get.k3s.io | K3S_URL=https://<MASTER_IP>:6443 K3S_TOKEN=<NODE_TOKEN> sh -``

  -confirmed cluster status with:
``sudo kubectl get nodes -o wide``

# 📋 Cluster Node Status

| NAME             | STATUS | ROLES                  | AGE   | VERSION     | INTERNAL-IP     | EXTERNAL-IP | OS-IMAGE           | KERNEL-VERSION     | CONTAINER-RUNTIME      |
|------------------|--------|-------------------------|-------|-------------|-----------------|-------------|--------------------|--------------------|------------------------|
| sor-k3s-master    | Ready  | control-plane,master    | 42m   | v1.32.3+k3s1 | ###.###.###.120   | <none>      | Ubuntu 24.04.2 LTS | 6.8.0-58-generic    | containerd://2.0.4-k3s2 |
| sor-k3s-worker1   | Ready  | <none>                  | 21s   | v1.32.3+k3s1 | ###.###.###.170   | <none>      | Ubuntu 24.04.2 LTS | 6.8.0-58-generic    | containerd://2.0.4-k3s2 |
| sor-k3s-worker2   | Ready  | <none>                  | 11m   | v1.32.3+k3s1 | ###.###.###.220   | <none>      | Ubuntu 24.04.2 LTS | 6.8.0-58-generic    | containerd://2.0.4-k3s2 |

## 🔑 Key Milestones

- ✅ Proxmox hosts installed and operational
- ✅ Ubuntu VMs spun up with static IPs
- ✅ K3s server installed on master node
- ✅ K3s agents installed on worker nodes
- ✅ Full cluster visible via `kubectl`
- ✅ SSH access confirmed on all nodes

---

## 🧠 Lessons Learned

- Always validate `node-token` during K3s worker join
- Ensure no conflicting services (like another K3s server) exist on workers
- Fix kubeconfig permissions early to avoid sudo frustration
- Troubleshoot agent joins by checking `journalctl -xeu k3s-agent`

---

## 📅 Transition to Week 2

Next steps:
- Deploy test workloads
- Configure Ingress Controller
- Explore Helm deployments
- Set up internal DNS and TLS
