# ⚙️ API/System Project Template

## Project Type Information

| Field | Value |
|-------|-------|
| **Type** | API / Backend System |
| **Complexity** | Medium / High |
| **Team Size** | 2-6 members typical |

---

## 1. Common Roles

| Role | Platform | Responsibilities |
|------|----------|------------------|
| **BE Developer** | Claude Code | API development |
| **DB Admin** | Claude Code | Database management |
| **DevOps** | OpenClaw | Infrastructure |
| **Security Engineer** | OpenClaw | Security, Auth |
| **QA Engineer** | Claude Code | API testing |
| **SA** | OpenClaw/Claude | Architecture |

---

## 2. Tech Stack Options

### API Frameworks
| Option | Use Case | Skills Required |
|--------|----------|-----------------|
| **Node.js + Express** | REST API | Node, Express |
| **NestJS** | Enterprise | TypeScript, NestJS |
| **FastAPI** | ML/AI APIs | Python, FastAPI |
| **Go + Gin** | High performance | Go, Gin |
| **Spring Boot** | Enterprise Java | Java, Spring |

### Database
| Option | Use Case |
|--------|----------|
| PostgreSQL | Relational |
| MongoDB | Document |
| Redis | Caching |
| Elasticsearch | Search |

### Message Queue
| Option | Use Case |
|--------|----------|
| RabbitMQ | Job queues |
| Redis Queue | Simple queues |
| Kafka | Event streaming |

---

## 3. Deployment Options

| Option | Complexity | Best For |
|--------|------------|----------|
| **VPS + Docker** | Medium | Full control |
| **Kubernetes** | High | Scalable systems |
| **Dokploy** | Low | Simple deployment |
| **AWS ECS/Fargate** | Medium | Managed containers |

---

## 4. Infrastructure Setup

### VPS Requirements
```yaml
minimum:
  cpu: 2 cores
  ram: 4GB
  storage: 50GB

production:
  cpu: 4+ cores
  ram: 8GB+
  storage: 100GB+
```

### Docker Services
```yaml
services:
  - api (port 8080)
  - database (port 5432)
  - redis (port 6379)
  - nginx (port 80/443)
  - monitoring (optional)
```

---

## 5. Security Checklist

- [ ] HTTPS enabled (Let's Encrypt)
- [ ] Rate limiting configured
- [ ] Input validation on all endpoints
- [ ] Authentication implemented
- [ ] Authorization checks
- [ ] SQL injection prevention
- [ ] CORS configured properly
- [ ] Secrets in vault, not code
- [ ] Logging without sensitive data
- [ ] Regular security updates

---

## 6. Credentials Needed

| Credential | Purpose | Storage |
|------------|---------|---------|
| SSH Key | Server access | Vault |
| DB Password | Database | .env |
| API Keys | External services | .env |
| JWT Secret | Auth tokens | .env |
| SSL Cert | HTTPS | Let's Encrypt |

---

## 7. API Documentation

### OpenAPI/Swagger
```yaml
documentation:
  - /api/docs (Swagger UI)
  - /api/spec (OpenAPI JSON)
```

### Endpoints Structure
```
/api/v1/
├── /auth
├── /users
├── /resources
└── /health
```

---

## 8. Git Branch Strategy

```
main (production)
  └── develop
        ├── feature/xxx
        ├── bugfix/xxx
        └── hotfix/xxx
```

---

## 9. Project Structure

```
project/
├── src/
│   ├── controllers/
│   ├── services/
│   ├── models/
│   ├── routes/
│   ├── middleware/
│   └── config/
├── tests/
├── docs/
│   ├── api/
│   └── meeting-notes/
├── docker-compose.yml
├── .env.example
└── README.md
```

---

## 10. Quick Start Checklist

- [ ] Create GitHub repo
- [ ] Setup VPS with SSH
- [ ] Configure Git authors
- [ ] Setup Docker environment
- [ ] Create .env from template
- [ ] Setup database
- [ ] Configure CI/CD
- [ ] Setup monitoring
- [ ] Configure security
- [ ] Add team members

---

*Template by Hina 🍀*