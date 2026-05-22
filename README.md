# Dynamic Multi-Project DevOps Pipeline with Namespace Isolation

## Project Overview

This project demonstrates the implementation of a complete multi-tenant DevOps pipeline using modern cloud-native technologies and automation tools.

The system automates infrastructure provisioning, configuration management, containerization, CI/CD, Kubernetes deployment, monitoring, and namespace isolation.

Multiple applications are deployed within a shared Kubernetes cluster while maintaining logical isolation using Kubernetes namespaces.

---

## Features

- Infrastructure provisioning using Terraform
- Configuration management using Ansible
- CI/CD automation using Jenkins
- Docker containerization
- Kubernetes orchestration
- Namespace isolation for multi-tenancy
- Prometheus monitoring
- Grafana dashboards
- Automated deployment pipeline
- AWS cloud deployment

---

## Architecture

The system follows a layered DevOps architecture:

GitHub → Jenkins → Docker → AWS ECR → Kubernetes → Monitoring Stack

### Components Used

| Tool | Purpose |
|------|----------|
| Terraform | Infrastructure provisioning |
| Ansible | Configuration management |
| Jenkins | CI/CD automation |
| Docker | Containerization |
| Kubernetes | Container orchestration |
| AWS EC2 | Cloud infrastructure |
| AWS ECR | Container registry |
| Prometheus | Monitoring |
| Grafana | Visualization |

---

## CI/CD Workflow

1. Developer pushes code to GitHub
2. Jenkins pipeline triggers automatically
3. Docker image is built
4. Image is pushed to AWS ECR
5. Kubernetes deployment is updated
6. Application becomes available through Ingress
7. Prometheus collects metrics
8. Grafana visualizes monitoring data

---

## Project Structure

```bash
.
├── terraform/
├── ansible/
├── kubernetes/
├── jenkins/
├── monitoring/
├── screenshots/
├── videos/
└── README.md
```

---

## Kubernetes Namespace Isolation

Each application is deployed inside its own namespace:

- project-a
- project-b
- project-c

This ensures:

- logical isolation
- resource separation
- independent deployments
- scalability

---

## Monitoring

Monitoring is implemented using:

- Prometheus
- Grafana

Metrics collected:

- CPU utilization
- Memory utilization
- Pod health
- Cluster performance

---

## Screenshots

### Jenkins Pipeline
![Jenkins](screenshots/jenkins-pipeline.png)

### Kubernetes Pods
![Pods](screenshots/kubernetes-pods.png)

### Grafana Dashboard
![Grafana](screenshots/grafana-dashboard.png)

### Prometheus Metrics
![Prometheus](screenshots/prometheus-query.png)

---

## Demo Videos

Demo videos of the live infrastructure and deployment process are included inside the `/videos` directory.

---

## Setup Commands

### Terraform

```bash
terraform init
terraform apply
```

### Ansible

```bash
ansible-playbook setup.yml
```

### Kubernetes Deployment

```bash
kubectl apply -f deployment.yaml
```

---

## Key Outcomes

- Reduced deployment time
- Automated infrastructure management
- Improved scalability
- Faster CI/CD workflow
- Namespace-based tenant isolation
- Real-time monitoring and observability

---

## Note

AWS infrastructure resources were terminated after project completion to avoid unnecessary cloud costs.

All deployment demonstrations, monitoring dashboards, and outputs were recorded and documented using screenshots and videos.
