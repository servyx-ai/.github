# Servyx

**AI-powered infrastructure intelligence for AWS & Kubernetes.**

Servyx analyzes your cloud infrastructure, detects waste, and provides actionable optimization recommendations — so you stop overpaying and start scaling smart.

## What Servyx Does

- **Discovers** your entire AWS infrastructure (EC2, EKS, RDS, and more)
- **Collects** Kubernetes cluster state (pods, deployments, nodes, resource usage)
- **Analyzes** costs with full billing and Cost Explorer integration
- **Recommends** optimizations with estimated savings and risk levels
- **Monitors** continuously with automated daily/hourly collection

## How It Works

1. **Connect your AWS account** — paste your read-only IAM credentials into Servyx. No binaries to install.
2. **Connect your Kubernetes clusters** — install our lightweight Helm chart. Read-only, runs as a CronJob.
3. **Get insights** — Servyx shows your infrastructure, costs, and optimization recommendations in a clean dashboard.

## Repositories

| Repo | Description | Visibility |
|------|-------------|------------|
| [servyx-nextjs](https://github.com/servyx-ai/servyx-nextjs) | Web platform & API | Private |
| [servyx-k8s-collector](https://github.com/servyx-ai/servyx-k8s-collector) | Kubernetes collector agent + Helm chart | Public |

## Security First

- AWS credentials are **encrypted at rest** with AES-256-GCM (unique key per account via HKDF)
- Kubernetes collector is **strictly read-only** — it can only `get` and `list` resources
- AWS IAM policy is **read-only** — no permissions to create, modify, or delete anything
- Collector tokens are **SHA-256 hashed** — raw tokens are never stored

## Tech Stack

- **Frontend**: Next.js 16, TypeScript, Tailwind CSS
- **Auth**: Firebase Authentication (Google Sign-In)
- **Database**: Supabase PostgreSQL + Prisma 7
- **AWS Collection**: Server-side via AWS SDK (no client-side binary)
- **K8s Collection**: Rust binary deployed as CronJob via Helm
- **Encryption**: AES-256-GCM with HKDF key derivation

---

Built by the Servyx team.
