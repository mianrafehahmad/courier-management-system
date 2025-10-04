# 🤖 factory.ai Agents Configuration

This file defines the AI agent responsibilities, environments, and module mappings
for the Courier Management System (factory-ai-courier-cms).

---

## 🧠 Agents Overview

| Agent Name | Description | Directory | Tech Stack |
|-------------|-------------|------------|-------------|
| `frontend-agent` | Builds and manages the Angular + Tailwind frontend | `/frontend` | Angular 18, TailwindCSS |
| `backend-agent` | Builds and maintains the Node.js / Express.js backend APIs | `/backend` | Node.js/Express.js, TypeORM, Redis, RabbitMQ |
| `infra-agent` | Handles Docker, Kubernetes, CI/CD, and deployment automation | `/infra` | Docker, K8s, GitHub Actions |
| `docs-agent` | Manages technical documentation, API specs, and readmes | `/docs` | Markdown, Swagger, Postman |

---

## ⚙️ Environments

- **Development:** local Docker Compose stack
- **Staging:** Kubernetes namespace `factory-staging`
- **Production:** Kubernetes namespace `factory-prod`
- **Secrets:** Managed via AWS Secrets Manager

---

## 📦 Modules to Build

1. **Authentication** — JWT + OAuth2 + RBAC
2. **User & Role Management**
3. **Shipment Management** — CRUD, tracking, barcode
4. **Warehouse Management** — inventory, transfers, RFID
5. **Finance** — COD, invoices, accounting integrations
6. **Notifications** — event-driven with RabbitMQ
7. **Analytics** — KPIs, dashboards, PDF/Excel export
8. **Ecommerce Integrations** — Shopify, WooCommerce, Magento

---

## 🔐 Security Policies

- Use HTTPS/TLS for all endpoints  
- Enforce JWT expiry and refresh  
- Sanitize input (XSS/SQLi prevention)  
- Implement role-based route guards  
- Log all admin/audit actions

---

## 🧱 Infrastructure Guidelines

- Containerize all services with Docker  
- Orchestrate via Kubernetes (K8s)  
- Use Redis for caching and sessions  
- Queue async events with RabbitMQ  
- Store assets in AWS S3  
- CI/CD via GitHub Actions

---

## ✅ Success Criteria

- Build passes lint/tests (≥80% coverage)
- CI pipeline succeeds
- Application runs end-to-end via `docker compose up`
- Swagger and frontend both load without errors
- Code deployed to staging environment

---

_This `agents.md` file tells factory.ai how to orchestrate code generation and updates across multiple agents and modules._
