# 📋 TỔNG HỢP FULL CONTEXT - Team Building Workflow System

## 🎯 Wi's Vision (2026-03-02)

### Mục tiêu chính:
Dùng OpenClaw build nhiều team cho các project khác nhau:
- Coding projects
- Testing/QA
- Outsource
- Startup
- Content (Facebook, blog...)
- Research

### Hina's Role:
- Thay Wi kiểm tra tiến độ
- Push team, validate work
- Báo cáo cho Wi

---

## 📐 Architecture đã thống nhất

```
Project-based Teams (KHÔNG phải Team A/B/C)

┌─────────────────┐  ┌─────────────────┐
│ Project: WebApp │  │ Project: Mobile │
├─────────────────┤  ├─────────────────┤
│ 🤖 Coder        │  │ 🤖 Dev          │
│ 🤖 QA           │  │ 🤖 QA           │
│ 👤 PM           │  │ 👤 PO           │
│ 👤 Client       │  │ 👤 Client       │
└─────────────────┘  └─────────────────┘

AI: 1 project only
Human: Multi-project (PM, PO, Client...)
```

---

## 🔄 Team Building Workflow (7 Steps)

```
Step 0: Wi + Hina discuss project idea
    ↓
Step 1 (OPTIONAL): Gather Advisors/Experts
    └─→ SA, TechLead, PM, BA...
    └─→ Khi chưa đủ thông tin để define
    ↓
Step 2: Define Project
    └─→ Project Charter Template
    └─→ Goals, scope, constraints, timeline
    ↓
Step 3: Identify Required Roles
    └─→ Role Definition Template
    └─→ FE Dev, BE Dev, QA, PM...
    ↓
Step 4: Build Team
    └─→ Subagent Template
    └─→ Create AI agents hoặc invite humans
    ↓
Step 5: Setup Team
    └─→ Role Map Template
    └─→ Team Workflow Template
    └─→ Assign members to roles
    ↓
Step 6: Onboard Members
    └─→ Onboarding Checklist
    ↓
Step 7: Start Execution
```

---

## 📁 7 Templates cần tạo

| # | Template | Purpose |
|---|----------|---------|
| 1 | Document tổng hợp workflows | Overview toàn bộ system |
| 2 | Project Charter Template | Define project mới |
| 3 | Role Definition Template | JD, skills, responsibilities |
| 4 | Subagent Template | Config tạo AI agent với role cụ thể |
| 5 | Role Map Template | Matrix role/responsibility trong team |
| 6 | Team Workflow Template | Collaboration flow giữa members |
| 7 | Onboarding Checklist | Checklist khi add member mới |

---

## 📋 Key Requirements

### Templates phải:
- ✅ Linh hoạt, có thể edit/customize
- ✅ Không build cứng
- ✅ Assign members trực tiếp vào roles
- ✅ Có guidelines cho team/member

### Reference từ agent-team repo:
- 9 roles: dev-fe, dev-be, designer, sa, tech-lead, devops, pm, ba, qa
- 50 skills across 9 categories
- Tool profiles: minimal, coding, research, orchestration, full
- Skill dependency system

---

## ✅ Completed

| Task | Status |
|------|--------|
| GitHub auth (gh) | ✅ hinavoid |
| Git setup | ✅ |
| Clone reference repo (agent-team) | ✅ |
| Research analysis | ✅ |
| Create 7 templates | ✅ |
| Push to GitHub | ✅ wipal/oc-team-workflow-research |

---

## 🔜 Next Steps

1. Review templates với Wi
2. Wi share role template đã build (để tham khảo)
3. Test với 4 models: qwen3-coder-plus, glm-5, kimi-k2.5, MiniMax-M2.5
4. Implement tool profiles trong OpenClaw config
5. Create role templates compatible với OpenClaw

---

*Created by Hina 🍀*
*Updated: 2026-03-04 11:55 UTC*