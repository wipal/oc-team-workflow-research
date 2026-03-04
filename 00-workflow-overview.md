# 📋 Workflow Overview - Team Building System

## 🏗️ Architecture Overview

### Multi-Platform / Multi-Vendor Architecture

```
Wi (Human Owner)
    ↓
Hina (Coordinator - OpenClaw)
    ↓
┌─────────────────────────────────────────────────────┐
│ PROJECT (Multi-Vendor)                              │
├─────────────────────────────────────────────────────┤
│ 📦 Claude Code                                      │
│    ├── 🤖 FE Dev Agent                             │
│    ├── 🤖 BE Dev Agent                             │
│    └── 🤖 QA Agent                                 │
│                                                     │
│ 📦 OpenClaw (Hina's subagents)                      │
│    ├── 🤖 Content Writer                           │
│    └── 🤖 SA (Solution Architect)                  │
│                                                     │
│ 📦 AntiGravity (Future)                             │
│    └── 🤖 Research Agent                           │
│                                                     │
│ 👤 Human: PM, PO, Client                           │
└─────────────────────────────────────────────────────┘
```

### Supported Platforms

| Platform | Best For | Skills Source |
|----------|----------|---------------|
| **Claude Code** | Code projects | agent-team templates |
| **OpenClaw** | General tasks, coordination | OpenClaw skills |
| **AntiGravity** | Research, analysis | Custom skills |
| **Other AI Apps** | Specific use cases | App-specific |

---

## Tổng Hợp Flow

### Step 0: Project Discussion
**Mục tiêu:** Hiểu rõ ý tưởng dự án

**Input:**
- Wi mô tả ý tưởng
- Context, constraints, goals

**Output:**
- Project understanding
- Initial scope

**Who:** Wi + Hina

---

### Step 1: Gather Advisors/Experts (OPTIONAL)
**Mục tiêu:** Thu thập expertise bổ sung

**Khi nào cần:**
- Project phức tạp
- Cần domain knowledge
- Technical challenges lớn

**Who có thể mời:**
- Solution Architect (SA)
- Tech Lead
- Project Manager (PM)
- Business Analyst (BA)
- Domain Experts

**Output:**
- Expert recommendations
- Risk assessment
- Technical direction

---

### Step 2: Define Project (Project Charter)
**Mục tiêu:** Định nghĩa rõ ràng project

**Template:** `01-project-charter.md`

**Nội dung:**
- Project name, description
- Goals & Objectives (SMART)
- Scope (In/Out)
- Stakeholders
- Timeline
- Budget
- Risks & Assumptions

**Who:** Wi + Hina (+ Advisors nếu có)

---

### Step 3: Identify Required Roles
**Mục tiêu:** Xác định vai trò cần thiết

**Template:** `02-role-definition.md`

**Nội dung:**
- Role name
- Responsibilities
- Required skills
- Time commitment
- AI vs Human decision

**Phân loại:**
| Type | Examples |
|------|----------|
| AI Roles | Coder, QA, Researcher, Writer |
| Human Roles | PM, Client, Stakeholder |
| Hybrid | Tech Lead, Architect |

---

### Step 4: Build Team
**Mục tiêu:** Setup team members

**Template:** `03-subagent-template.md`

**Cho AI Agents:**
- Configure agent
- Define capabilities
- Setup tools
- Test agent

**Cho Humans:**
- Recruit/invite
- Share project info
- Schedule kickoff

---

### Step 5: Setup Team
**Mục tiêu:** Tổ chức team

**Templates:**
- `04-role-map.md` - Ai làm gì
- `05-team-workflow.md` - Quy trình

**Nội dung:**
- RACI matrix
- Communication channels
- Meeting schedule
- Reporting structure
- Escalation paths

---

### Step 6: Onboard Members
**Mục tiêu:** Đưa members vào project

**Template:** `06-onboarding-checklist.md`

**Nội dung:**
- Access setup
- Documentation
- Tools access
- Intro meetings
- First tasks

---

### Step 7: Start Execution
**Mục tiêu:** Bắt đầu làm việc

**Activities:**
- Daily standups
- Sprint planning (nếu dùng Agile)
- Progress tracking
- Regular reviews

---

## 🔄 Iteration

Flow có thể lặp lại:
- Add new roles → Step 3
- Change scope → Step 2
- New member → Step 6

---

## 📊 Decision Matrix: AI vs Human

| Criteria | AI Agent | Human |
|----------|----------|-------|
| Repetitive tasks | ✅ | ❌ |
| Creative decisions | ⚠️ | ✅ |
| 24/7 availability | ✅ | ❌ |
| Complex judgment | ⚠️ | ✅ |
| Client interaction | ❌ | ✅ |
| Code generation | ✅ | ⚠️ |
| Strategic decisions | ❌ | ✅ |

---

*Created by Hina 🍀*