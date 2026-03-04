# 🗺️ Role Map Template

## Project Information

| Field | Value |
|-------|-------|
| **Project Name** | [Tên project] |
| **Last Updated** | [YYYY-MM-DD] |
| **Version** | 1.0 |

---

## 1. Team Overview

### Team Structure
```
                    ┌─────────┐
                    │   Wi    │ (Sponsor/Owner)
                    └────┬────┘
                         │
                    ┌────┴────┐
                    │  Hina   │ (PM/Coordinator)
                    └────┬────┘
                         │
        ┌────────────────┼────────────────┐
        │                │                │
   ┌────┴────┐     ┌────┴────┐     ┌────┴────┐
   │ Agent A │     │ Agent B │     │ Human C │
   │ (Coder) │     │  (QA)   │     │  (SA)   │
   └─────────┘     └─────────┘     └─────────┘
```

---

## 2. RACI Matrix

| Task/Decision | Wi | Hina | Agent A | Agent B | Human C |
|---------------|-----|------|---------|---------|---------|
| Project Direction | A | R | I | I | C |
| Code Development | I | I | R | C | I |
| Code Review | I | I | C | R | I |
| Architecture | A | C | C | I | R |
| Deployment | I | A | R | C | I |

**Legend:**
- **R** = Responsible (Who does the work)
- **A** = Accountable (Who approves/signs off)
- **C** = Consulted (Who provides input)
- **I** = Informed (Who needs to know)

---

## 3. Role Assignments

### AI Agents

| Agent ID | Role | Model | Purpose | Status |
|----------|------|-------|---------|--------|
| code-agent | Developer | qwen3-coder-next | Code, debug | ✅ Active |
| qa-agent | QA | glm-4.7 | Testing, review | ✅ Active |
| [agent-id] | [Role] | [Model] | [Purpose] | [Status] |

### Humans

| Name | Role | Skills | Availability | Contact |
|------|------|--------|--------------|---------|
| Wi | Sponsor/Owner | [Skills] | On-demand | Telegram |
| [Name] | [Role] | [Skills] | [Hours/week] | [Contact] |

---

## 4. Communication Map

### Channels

| Channel | Purpose | Members |
|---------|---------|---------|
| Telegram (Main) | Primary communication | Wi, Hina |
| Slack #project | Team discussions | All |
| GitHub | Code, issues | Dev agents |

### Communication Matrix

| From → To | Wi | Hina | Agent A | Agent B |
|-----------|-----|------|---------|---------|
| **Wi** | - | Telegram | Via Hina | Via Hina |
| **Hina** | Telegram | - | Spawn | Spawn |
| **Agent A** | Via Hina | Reply | - | Direct |
| **Agent B** | Via Hina | Reply | Direct | - |

---

## 5. Decision Authority

| Decision Type | Authority Level | Who Decides |
|---------------|-----------------|-------------|
| Project scope | High | Wi |
| Technical approach | Medium | Hina + SA |
| Code implementation | Low | Code Agent |
| Release | High | Wi + Hina |
| Hiring/Adding agents | Medium | Hina → Wi approval |

---

## 6. Escalation Paths

### Level 1: Agent → Agent
```
Agent detects issue → Attempts resolution → 
If unresolved in [X] attempts → Escalate to Hina
```

### Level 2: Agent → Hina
```
Hina receives escalation → Analyzes → 
Resolves or → Escalate to Wi
```

### Level 3: Hina → Wi
```
Wi makes final decision → Hina implements
```

### Escalation Triggers
- [ ] Error rate > 10%
- [ ] Task stuck > 2 hours
- [ ] Scope creep detected
- [ ] Resource conflict
- [ ] [Custom trigger]

---

## 7. Handoff Protocol

### Agent-to-Agent Handoff
```yaml
handoff:
  from: [agent-id]
  to: [agent-id]
  include:
    - task_summary
    - context
    - files_modified
    - blockers
  format: structured_json
```

### Human-to-Agent Handoff
```yaml
handoff:
  from: [human-name]
  to: [agent-id]
  include:
    - requirements
    - constraints
    - deadline
    - priority
```

---

## 8. Availability Schedule

### Human Availability

| Person | Timezone | Available Hours | Notes |
|--------|----------|-----------------|-------|
| Wi | GMT+7 | Flexible | On-demand |
| [Name] | [TZ] | [Hours] | [Notes] |

### Agent Availability

| Agent | Availability | Limitations |
|-------|--------------|-------------|
| All agents | 24/7 | Rate limits apply |

---

## 9. Backup & Coverage

### Primary/Backup Assignments

| Role | Primary | Backup |
|------|---------|--------|
| PM | Hina | [Agent] |
| Coder | code-agent | qwen3-coder-plus |
| QA | qa-agent | [Backup agent] |

### Coverage During Absence
```
If [Person] unavailable:
- [Task type] → [Backup person/agent]
- [Task type] → [Backup person/agent]
```

---

## 10. Skills Matrix

| Person/Agent | Code | Test | Research | Writing | PM | Architecture |
|--------------|------|------|----------|---------|-----|--------------|
| Wi | - | - | - | - | ⭐ | ⭐ |
| Hina | ⭐ | ⭐ | ⭐ | ⭐ | ⭐ | ⭐ |
| code-agent | ⭐⭐⭐ | ⭐ | ⭐ | - | - | ⭐ |
| qa-agent | ⭐ | ⭐⭐⭐ | - | - | - | - |

**Legend:**
- ⭐⭐⭐ = Expert
- ⭐⭐ = Proficient
- ⭐ = Basic
- - = Not applicable

---

*Template by Hina 🍀*