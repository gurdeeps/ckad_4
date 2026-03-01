# EKS Cluster Setup: my-ckad-cluster

This guide provides instructions for spinning up a managed Kubernetes cluster on AWS EKS using `eksctl`. This setup is optimized for CKAD (Certified Kubernetes Application Developer) practice.

## 🛠 Prerequisites

Before starting, ensure you have the following tools installed and configured:
* **AWS CLI**: Configured with appropriate IAM permissions.
* **eksctl**: The official CLI tool for Amazon EKS.
* **kubectl**: The Kubernetes command-line tool.

---

## 🚀 1. Provision the Cluster

Run the following command to create the cluster. 
> **Note:** This process typically takes **15–20 minutes** as AWS provisions the Control Plane, VPC, and Node Groups.

```bash
eksctl create cluster --name my-ckad-cluster --nodes 2 --node-type m5.large --region us-east-1
```

## 🚀 2. Download/Update Kubeconfig

```bash
aws eks update-kubeconfig --region us-east-1 --name my-ckad-cluster
```

