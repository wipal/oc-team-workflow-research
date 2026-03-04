# 🌐 Web App Project Template

## Project Type Information

| Field | Value |
|-------|-------|
| **Type** | Web Application |
| **Complexity** | Low / Medium / High |
| **Team Size** | 2-8 members typical |

---

## 1. Common Roles

| Role | Platform | Responsibilities |
|------|----------|------------------|
| **FE Developer** | Claude Code | UI/UX implementation |
| **BE Developer** | Claude Code | API, Database, Logic |
| **QA Engineer** | Claude Code | Testing, Automation |
| **DevOps** | OpenClaw | Deployment, CI/CD |
| **PM** | Human | Project management |
| **SA** | OpenClaw/Claude | Architecture |

---

## 2. Tech Stack Options

### Frontend
| Option | Use Case | Skills Required |
|--------|----------|-----------------|
| React + TypeScript | SPA, Complex UI | React, TS, State mgmt |
| Vue 3 | Lightweight SPA | Vue, Composition API |
| Next.js | SEO, SSR | React, Next.js |
| Angular | Enterprise | Angular, RxJS |

### Backend
| Option | Use Case | Skills Required |
|--------|----------|-----------------|
| Node.js + Express | REST API | Node, Express, DB |
| NestJS | Enterprise API | NestJS, TypeScript |
| Python + FastAPI | ML/AI features | Python, FastAPI |
| Go | High performance | Go, Gin/Echo |

### Database
| Option | Use Case |
|--------|----------|
| PostgreSQL | Relational data |
| MongoDB | Document store |
| Redis | Caching, Sessions |
| Supabase | Backend-as-a-Service |

---

## 3. Deployment Options

| Option | Complexity | Cost | Best For |
|--------|------------|------|----------|
| **VPS + Docker** | Medium | Low | Full control |
| **VPS + Dokploy** | Low | Low | Easy deployment |
| **GitHub Actions** | Medium | Free tier | CI/CD automation |
| **Vercel/Netlify** | Low | Freemium | Frontend only |
| **AWS/GCP/Azure** | High | Variable | Enterprise |

---

## 4. Infrastructure Setup

### VPS Requirements
```yaml
minimum:
  cpu: 2 cores
  ram: 4GB
  storage: 40GB SSD
  
recommended:
  cpu: 4 cores
  ram: 8GB
  storage: 80GB SSD
```

### Docker Setup
```yaml
services:
  - frontend (port 3000)
  - backend (port 8080)
  - database (port 5432)
  - redis (port 6379)
  - nginx (port 80/443)
```

### GitHub Actions
```yaml
workflows:
  - ci.yml (test, lint)
  - cd.yml (deploy)
  - pr.yml (PR checks)
```

---

## 5. Credentials Needed

| Credential | Purpose | Storage |
|------------|---------|---------|
| SSH Key | Server access | Vault |
| DB Password | Database | .env |
| API Keys | External services | .env |
| SSL Cert | HTTPS | Let's Encrypt |
| Git Token | CI/CD | GitHub Secrets |

---

## 6. Git Branch Strategy

```
main (production)
  └── develop (staging)
        ├── feature/xxx
        ├── bugfix/xxx
        └── hotfix/xxx
```

### Commit Convention
```
[Agent-Name] type: message

Examples:
[FE-Dev] feat: add login page
[BE-Dev] fix: resolve API timeout
[QA] test: add e2e tests for checkout
```

---

## 7. Project Structure

```
project/
├── frontend/
│   ├── src/
│   ├── public/
│   ├── tests/
│   └── package.json
├── backend/
│   ├── src/
│   ├── tests/
│   └── package.json
├── docs/
│   └── meeting-notes/
├── docker-compose.yml
├── .env.example
└── README.md
```

---

## 8. Meeting Notes

All meetings stored in: `/docs/meeting-notes/`

Format: `YYYY-MM-DD-[topic].md`

See: `08-meeting-notes-template.md`

---

## 9. Quick Start Checklist

- [ ] Create GitHub repo
- [ ] Setup VPS with SSH
- [ ] Configure Git authors per agent
- [ ] Setup Docker environment
- [ ] Create .env from template
- [ ] Configure GitHub Actions
- [ ] Setup meeting notes folder
- [ ] Add team members to project

---

*Template by Hina 🍀*