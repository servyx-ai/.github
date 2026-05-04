# Servyx

**AI-powered infrastructure intelligence for AWS & Kubernetes.**

Servyx analyzes your cloud infrastructure, detects waste, and provides actionable optimization recommendations — so you stop overpaying and start scaling smart.

## What Servyx Does

- **Discovers** your entire AWS infrastructure (EC2, EKS, RDS, and more)
- **Collects** Kubernetes cluster state (pods, deployments, nodes, resource usage)
- **Analyzes** costs with full billing and Cost Explorer integration
- **Recommends** optimizations with estimated savings and risk levels
- **Monitors** continuously with automated collection

## How It Works

1. **Connect your AWS account** — read-only access, no binaries to install
2. **Connect your Kubernetes clusters** — lightweight Helm chart, read-only
3. **Get insights** — infrastructure, costs, and optimization recommendations in a clean dashboard

## Open Source

| Repo | Description |
|------|-------------|
| [servyx-k8s-collector](https://github.com/servyx-ai/servyx-k8s-collector) | Kubernetes collector agent + Helm chart |

## Security

- All credentials are **encrypted at rest** with unique keys per account
- All collectors are **strictly read-only** — no permissions to modify anything
- Authentication tokens are **hashed** — raw tokens are never stored

---

Built by the Servyx team.
