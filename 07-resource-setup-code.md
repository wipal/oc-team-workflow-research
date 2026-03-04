# 🔧 Resource Setup Template - Code Projects

## Project Information

| Field | Value |
|-------|-------|
| **Project Name** | [Tên dự án] |
| **Project Type** | Web App / Mobile App / API / Other |
| **Created Date** | [YYYY-MM-DD] |
| **Platform** | Claude Code / OpenClaw / Other |

---

## 1. Git Configuration

### Git Account
```yaml
account: Hina (hinavoid)
email: hinavoidass@gmail.com
ssh_key: ssh-ed25519 AAAAC3NzaC1lZDI1NTE5AAAAIP+6qfFvD4VQvJVWzSldp0i/QqxgN+jQ5hjNvJrPLQX9
```

### Author Configuration (Per Agent)
```bash
# Each agent commits with their own author
git config user.name "[Agent Name] ([Role])"
git config user.email "[agent-name]@[project].hina"

# Example:
# git config user.name "Coder-Bot (FE Dev)"
# git config user.email "coder-bot@ecommerce.hina"
```

### Repository Structure
```
project-repo/
├── .git/
├── src/
├── docs/
├── .env.example
└── README.md
```

---

## 2. SSH Configuration

### SSH Keys
```yaml
# Hina's SSH key (shared)
default_key: ~/.ssh/id_ed25519

# Project-specific key (optional)
project_key: ~/.ssh/[project-name]_ed25519
```

### SSH Config
```bash
# ~/.ssh/config
Host github.com-[project-name]
  HostName github.com
  User git
  IdentityFile ~/.ssh/[project-name]_ed25519
```

---

## 3. Credentials Vault

### Storage Location
```yaml
vault_path: /data/workspace/.secrets/[project-name]/
```

### Credentials Structure
```
.secrets/[project-name]/
├── .env              # Environment variables
├── db-credentials.json
├── api-keys.json
├── ssh-keys/
│   └── deploy_key
└── README.md         # What each credential is for
```

### .env Template
```bash
# Database
DB_HOST=
DB_PORT=
DB_NAME=
DB_USER=
DB_PASSWORD=

# API Keys
API_KEY_STRIPE=
API_KEY_SENDGRID=

# App Settings
APP_ENV=development
APP_DEBUG=true
APP_SECRET=

# Git
GIT_AUTHOR_NAME="[Agent Name]"
GIT_AUTHOR_EMAIL="[agent]@[project].hina"
```

---

## 4. Environment Variables

### Development
```bash
NODE_ENV=development
DATABASE_URL=postgresql://...
REDIS_URL=redis://...
```

### Staging
```bash
NODE_ENV=staging
DATABASE_URL=postgresql://...
```

### Production
```bash
NODE_ENV=production
# Never store in git - use secure vault
```

---

## 5. Platform-Specific Setup

### Claude Code Setup
```yaml
# .claude/ structure
.claude/
├── CLAUDE.md          # Project instructions
├── agents/            # Agent configs
│   ├── fe-dev.md
│   ├── be-dev.md
│   └── qa.md
├── skills/            # Custom skills
└── commands/          # Custom commands
```

### OpenClaw Setup
```yaml
# Subagent config
agents:
  - id: [project]-[role]
    model: bailian/qwen3-coder-plus
    workspace: /data/workspace/[project]/
```

---

## 6. Communication Integration

### Telegram Integration
```yaml
# Option A: Via Hina (Recommended)
method: hina-bridge
coordinator: Hina
channel: Telegram

# Option B: Direct (If supported)
method: direct
bot_token: [stored in vault]
allowed_agents:
  - [agent-id-1]
  - [agent-id-2]
```

### Message Routing
```
Human → Telegram → Hina → Agent
Agent → Hina → Telegram → Human
```

---

## 7. Access Control

### Agent Permissions Matrix

| Resource | FE Dev | BE Dev | QA | Tech Lead |
|----------|--------|--------|-----|-----------|
| Git Repo | ✅ RW | ✅ RW | ✅ R | ✅ RW |
| Database | ❌ | ✅ RW | ✅ R | ✅ R |
| API Keys | ❌ | ✅ R | ❌ | ✅ R |
| Deploy | ❌ | ❌ | ❌ | ✅ |

### Human Roles
| Resource | PM | Client | SA |
|----------|-----|--------|-----|
| Git Repo | ✅ R | ❌ | ✅ RW |
| Reports | ✅ RW | ✅ R | ✅ RW |
| Dashboard | ✅ RW | ✅ R | ✅ RW |

---

## 8. Monitoring & Logging

### Activity Log
```yaml
log_path: /data/workspace/[project]/logs/
log_types:
  - commits
  - deployments
  - agent-activities
  - errors
```

### Metrics to Track
- Commits per agent
- Tasks completed
- Errors encountered
- Response times

---

## 9. Backup & Recovery

### Backup Schedule
```yaml
database: daily
code: on-commit (git)
credentials: on-change (encrypted)
```

### Recovery Procedures
1. Database restore from backup
2. Git revert/rollback
3. Credential rotation

---

## 10. Security Checklist

- [ ] SSH keys generated and added to platforms
- [ ] Credentials stored in vault (not in git)
- [ ] .gitignore includes .env, credentials
- [ ] Agent permissions configured
- [ ] Telegram integration tested
- [ ] Git author config per agent
- [ ] Backup schedule set

---

## 11. Quick Setup Commands

### Initialize Project
```bash
# Create project structure
mkdir -p /data/workspace/[project]
cd /data/workspace/[project]

# Initialize git
git init
git remote add origin [repo-url]

# Create .env from template
cp templates/.env.example .env

# Setup git author
git config user.name "[First Agent] ([Role])"
git config user.email "[agent]@[project].hina"
```

### Add New Agent
```bash
# Set agent-specific author
git config user.name "[New Agent] ([Role])"
git config user.email "[new-agent]@[project].hina"

# Or use per-commit author
git commit --author="[Agent] ([Role]) <[agent]@[project].hina>"
```

---

*Template by Hina 🍀*
*Last Updated: 2026-03-04*