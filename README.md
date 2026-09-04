# Employee Directory - Kubernetes Continuation & Learning Lab

> **Continuation of the Employee Directory DevOps project**
>
> This repository is a Kubernetes-focused continuation of my original
> Employee Directory project. The application itself was previously
> containerized and deployed using Docker, Docker Compose, GitHub Actions,
> Docker Hub, and Jenkins.
>
> For this stage, I created a separate Kubernetes lab environment using
> dedicated VMs and rebuilt the deployment using Kubernetes to understand
> container orchestration in practice.
>
> This repository is primarily a **learning and hands-on lab project**,
> rather than a replacement for the original application repository.

## Project Progression

This project was developed in stages.

### Previous Repository

**Employee Directory — Docker & CI/CD**

The original project focused on:

- Linux server administration
- Nginx and Apache
- Docker
- Docker Compose
- PostgreSQL
- GitHub Actions
- Trivy
- Docker Hub
- Jenkins
- CI/CD

### This Repository

**Employee Directory — Kubernetes**

This stage focuses on:

- Kubernetes cluster architecture
- kubeadm
- Control plane and worker nodes
- Pods
- Deployments
- ReplicaSets
- Services
- ConfigMaps
- Secrets
- PersistentVolumes
- PersistentVolumeClaims
- PostgreSQL persistent storage
- Ingress
- NGINX Ingress Controller
- Health probes
- Scaling
- Rolling updates
- Rollbacks
- Kubernetes troubleshooting

The goal of this repository was to take the existing containerized
application and understand how it can be deployed and operated using
Kubernetes.

---
---
## Lab Environment

The Kubernetes environment was created separately from the original
application environment.

### Kubernetes Cluster

| Node | Role |
|---|---|
| k8s-master | Kubernetes control plane |
| k8s-worker1 | Worker node |
| k8s-worker2 | Worker node |

The cluster was created using `kubeadm`.

### Infrastructure

- Proxmox
- Ubuntu Server VMs
- pfSense
- Kubernetes
- NGINX Ingress Controller