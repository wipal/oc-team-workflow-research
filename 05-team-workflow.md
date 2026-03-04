# 🔄 Team Workflow Template

## Project Information

| Field | Value |
|-------|-------|
| **Project Name** | [Tên project] |
| **Methodology** | Agile / Waterfall / Hybrid |
| **Sprint Length** | [1-2 weeks] |
| **Last Updated** | [YYYY-MM-DD] |

---

## 1. Workflow Overview

### High-Level Flow
```
┌─────────┐   ┌─────────┐   ┌─────────┐   ┌─────────┐
│  Plan   │ → │  Build  │ → │  Test   │ → │ Deploy  │
└─────────┘   └─────────┘   └─────────┘   └─────────┘
     ↑                                          │
     └──────────────────────────────────────────┘
                     Iterate
```

---

## 2. Daily Workflow

### Morning (Start of Day)

| Time | Activity | Who | Duration |
|------|----------|-----|----------|
| 09:00 | Check overnight results | Hina | 10 min |
| 09:10 | Review blockers | Hina + Agents | 15 min |
| 09:30 | Start tasks | All | - |

### During Day

| Activity | Who | Frequency |
|----------|-----|-----------|
| Task execution | Agents | Continuous |
| Progress updates | Hina | Every 2h |
| Issue resolution | Hina | As needed |
| Human check-ins | Wi | On-demand |

### End of Day

| Activity | Who | Duration |
|----------|-----|----------|
| Status summary | Hina | 10 min |
| Save state | All | 5 min |
| Plan next day | Hina | 10 min |

---

## 3. Sprint Workflow (If Agile)

### Sprint Cycle
```
Day 1: Sprint Planning
Day 2-N: Development
Day N-1: Testing & Fixes
Day N: Sprint Review + Retro
```

### Sprint Planning

| Step | Who | Output |
|------|-----|--------|
| 1. Review backlog | Wi + Hina | Prioritized items |
| 2. Estimate effort | Agents | Story points |
| 3. Commit to sprint | All | Sprint backlog |
| 4. Assign tasks | Hina | Task assignments |

### Daily Standup (Async)

**Format:**
```
Yesterday: [What was done]
Today: [What will be done]
Blockers: [Any issues]
```

**Who reports:**
- Hina (summary of all agents)
- Human team members (direct)

### Sprint Review

| Step | Who | Duration |
|------|-----|----------|
| Demo completed work | Agents | 20 min |
| Stakeholder feedback | Wi | 10 min |
| Accept/Reject items | Wi | 5 min |

### Sprint Retrospective

**Questions:**
- What went well?
- What could improve?
- Action items for next sprint?

---

## 4. Task Workflow

### Task Lifecycle
```
┌──────────┐
│  Backlog │
└────┬─────┘
     │ Pull
     ↓
┌──────────┐
│  Ready   │
└────┬─────┘
     │ Start
     ↓
┌──────────┐
│In Progress│
└────┬─────┘
     │ Complete
     ↓
┌──────────┐
│  Review  │
└────┬─────┘
     │ Approve
     ↓
┌──────────┐
│  Done    │
└──────────┘
```

### Task States

| State | Meaning | Who Can Move |
|-------|---------|--------------|
| Backlog | Not started | Hina, Wi |
| Ready | Ready to work | Hina |
| In Progress | Being worked on | Agent |
| Review | Needs review | QA Agent |
| Done | Completed & approved | Hina, Wi |
| Blocked | Cannot proceed | Any → Hina |

---

## 5. Code Workflow

### Git Flow
```
main (protected)
  │
  ├── develop
  │     │
  │     ├── feature/TICKET-123
  │     │
  │     └── feature/TICKET-456
  │
  └── release/v1.0
```

### Branch Naming
```
feature/TICKET-123-short-description
bugfix/TICKET-456-bug-description
hotfix/TICKET-789-critical-fix
```

### Commit Message Format
```
[TICKET-123] Short description

- Detail 1
- Detail 2
```

### PR/Review Process

| Step | Who | Duration |
|------|-----|----------|
| Create PR | Coder Agent | - |
| Auto-review | QA Agent | 5 min |
| Human review | Wi (if needed) | 30 min |
| Merge | Hina | 1 min |

---

## 6. Communication Protocols

### Sync vs Async

| Type | When | Tools |
|------|------|-------|
| Sync | Urgent, complex discussions | Telegram call |
| Async | Most work, updates | Telegram messages |

### Message Priority

| Priority | Response Time | Examples |
|----------|---------------|----------|
| 🔴 Critical | < 15 min | Production down, data loss |
| 🟡 High | < 2 hours | Blocked task, deadline at risk |
| 🟢 Normal | < 1 day | Regular updates, questions |

### Notification Rules

```
Notify Wi when:
- Critical error
- Decision needed
- Milestone reached
- Budget alert

Don't notify Wi when:
- Normal operations
- Self-resolving issues
- Progress updates (unless asked)
```

---

## 7. Meeting Schedule

| Meeting | Frequency | Who | Duration | Purpose |
|---------|-----------|-----|----------|---------|
| Standup | Daily | Hina → Wi | 5 min | Status update |
| Sprint Planning | Bi-weekly | All | 30 min | Plan sprint |
| Sprint Review | Bi-weekly | All | 30 min | Demo work |
| 1:1 | Weekly | Wi + Hina | 15 min | Sync |

---

## 8. Quality Gates

### Code Quality
- [ ] Code compiles
- [ ] Unit tests pass
- [ ] No critical vulnerabilities
- [ ] Code reviewed

### Deployment Quality
- [ ] Tests pass in staging
- [ ] Documentation updated
- [ ] Rollback plan ready

---

## 9. Automation Rules

### Auto-Actions
```yaml
on_task_complete:
  - update_status: "Review"
  - notify: "Hina"
  - run_tests: true

on_error:
  - retry: 3
  - escalate_to: "Hina"
  - log_error: true

on_blocker:
  - notify: "Hina"
  - suggest_alternatives: true
```

### Scheduled Jobs
```yaml
daily:
  - time: "09:00"
    task: "check_progress"
  - time: "18:00"
    task: "send_summary"
```

---

## 10. Reporting

### Daily Report (To Wi)
```
📊 Daily Summary - [Date]

✅ Completed:
- [Item 1]
- [Item 2]

🔄 In Progress:
- [Item 3] - 50%

⚠️ Blockers:
- [Issue] - [Status]

📅 Tomorrow:
- [Plan 1]
```

### Weekly Report
```
📊 Week [N] Summary

📈 Progress: [X]% complete
✅ Completed: [N] tasks
🔄 In Progress: [N] tasks
⚠️ Blockers: [N] issues
💰 Budget: [Status]

🎯 Next Week Goals:
- [Goal 1]
- [Goal 2]
```

---

*Template by Hina 🍀*