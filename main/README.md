# 🚀 Kubernetes Homelab Project

## 🎯 Project Overview

This project is a self-hosted, Proxmox-based Kubernetes homelab designed to simulate enterprise production environments.  
It focuses on developing practical skills in:

- Kubernetes deployment and management (K3s)
- GitOps workflows
- Helm package management
- Ingress and service routing
- Monitoring and observability
- RBAC and security policies
- Backup and resilience strategies

The objective is to achieve **working, production-aligned competency** in Kubernetes operations suitable for professional DevOps, SRE, and Platform Engineering roles.

---

## 🛠️ Environment Setup

| Component       | Details                            |
|-----------------|-------------------------------------|
| Hypervisor      | Proxmox VE across three physical nodes |
| Virtualization  | 1x Ubuntu 24.04 Server VM per node  |
| Kubernetes      | K3s lightweight Kubernetes (v1.32.3+k3s1) |
| Container Runtime | containerd (via K3s)               |
| Networking      | Static IP addresses |
| Management Tools| kubectl, k9s, Helm                   |
| Access Method   | SSH with password authentication enabled |

---

## 📋 Current Cluster Topology

| Node Name         | Role                   | OS Image           |
|-------------------|------------------------|--------------------|
| sor-k3s-master     | control-plane, master  | Ubuntu 24.04.2 LTS |
| sor-k3s-worker1    | worker                 | Ubuntu 24.04.2 LTS |
| sor-k3s-worker2    | worker                 | Ubuntu 24.04.2 LTS |

---

## 📋 Project Phases Overview

**Phase 1:** Cluster Setup and Baseline Tools  
**Phase 2:** Application Deployment and Routing (Ingress, Services)  
**Phase 3:** GitOps Implementation (ArgoCD)  
**Phase 4:** Monitoring and Metrics (Prometheus, Grafana)  
**Phase 5:** Security Hardening (RBAC, Network Policies)  
**Phase 6:** Backup, Disaster Recovery, and Documentation

---

## 🧠 Learning Objectives

By the end of this project:

- Demonstrate ability to build and manage Kubernetes clusters
- Automate deployments using Helm and GitOps
- Implement observability and security best practices
- Operate a resilient, multi-node Kubernetes environment
