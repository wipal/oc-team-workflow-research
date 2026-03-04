# 📋 TỔNG HỢP NGHIÊN CỨU - Team Building Workflow System

## 🔍 Context từ 30 messages

### Nhiệm vụ chính:
1. Nghiên cứu và lập plan chi tiết cho từng step/template
2. Lưu vào git repo
3. Tài liệu cấu trúc và dynamic
4. Tham khảo repo: https://github.com/wipal/agent-team
5. Xem xét options: subagent vs standalone app
6. Note những phần chưa rõ
7. Tạo bảng so sánh
8. Implement với 4 model khác nhau

---

## 📊 Phân tích Reference Repo: agent-team

### Kiến trúc chính:
```
Base Role + Variants System
├── Base Role (dev-fe, dev-be, designer, sa, tech-lead, devops, pm, ba, qa)
├── Variants (React, Vue, Angular, Vanilla)
├── Tool Profiles (minimal, coding, research, orchestration, full)
└── Capability-Based Security
```

### 9 Roles có sẵn:
| Role | Tool Profile | Skills | Description |
|------|--------------|--------|-------------|
| dev-fe | coding | 11 | Frontend Developer |
| dev-be | coding | 10 | Backend Developer |
| designer | minimal | 10 | UI/UX Designer |
| sa | full | 13 | Solution Architect |
| tech-lead | orchestration | 20 | Tech Lead (inherits dev-fe + dev-be) |
| devops | coding | 10 | DevOps Engineer |
| pm | research | 11 | Product Manager |
| ba | research | 11 | Business Analyst |
| qa | coding | 9 | QA Engineer |

### Tool Profiles:
| Profile | Tools | Used By |
|---------|-------|---------|
| minimal | read, write, edit | designer |
| coding | + bash, grep, glob + filesystem, github | dev-fe, dev-be, devops, qa |
| research | + web_search, web_fetch + context7, docs-seeker | pm, ba |
| orchestration | coding + task + context7 | tech-lead |
| full | all tools + all MCP servers | sa |

### 50 Skills trong 9 categories:
- Core (5): code-review, git-automation, retrospect, agent-creation, sequential-thinking
- Frontend (6): React/Vue/UI development
- Backend (5): API/Database/Security
- Design (5): UI design, design systems, mockups
- Architecture (8): System design, ADRs, C4, Mermaid
- DevOps (5): CI/CD, Docker, Terraform
- Product (6): Requirements, Sprints
- Quality (4): Testing, QA
- Leadership (4): Tech Lead skills

---

## 🔄 So sánh: Subagent vs Standalone App

| Criteria | Subagent (OpenClaw) | Standalone (Claude Code/AntiGravity) |
|----------|---------------------|--------------------------------------|
| **Setup** | ✅ Nhanh, trong config | ⚠️ Cần setup riêng |
| **Communication** | ✅ Tự động qua spawn | ⚠️ Cần API/hook |
| **Cost** | ✅ Chia sẻ resources | ❌ Resource riêng |
| **Isolation** | ⚠️ Chia sẻ workspace | ✅ Workspace riêng |
| **Flexibility** | ⚠️ Giới hạn tools | ✅ Tùy chỉnh hoàn toàn |
| **Model switching** | ✅ Built-in routing | ❌ Cần tự implement |
| **Knowledge sharing** | ✅ Memory chung | ⚠️ Cần sync thủ công |
| **Scalability** | ⚠️ Giới hạn concurrent | ✅ Unlimited |
| **Best for** | Team nhỏ, dự án gọn | Team lớn, dự án phức tạp |

### 🎯 Recommendation:
- **Mặc định:** Dùng Subagent (OpenClaw) - phù hợp 90% use cases
- **Khi nào dùng Standalone:**
  - Dự án cần isolation cao
  - Nhiều external integrations
  - Team > 10 agents

---

## 📋 PLAN TỔNG HỢP

### Phase 1: Foundation (Done ✅)
- [x] 7 Templates cơ bản
- [x] Research reference repo
- [x] Clone reference repo

### Phase 2: Research & Analysis
- [ ] Phân tích chi tiết 50 skills từ agent-team
- [ ] Map skills → OpenClaw capabilities
- [ ] Tạo skill dependency graph
- [ ] Document architecture patterns

### Phase 3: Integration
- [ ] Implement tool profiles trong OpenClaw config
- [ ] Create role templates compatible với OpenClaw
- [ ] Setup memory system per agent
- [ ] Implement skill inheritance

### Phase 4: Testing với 4 Models
- [ ] qwen3-coder-plus: Code tasks
- [ ] glm-5: Analysis tasks
- [ ] kimi-k2.5: Creative/Research
- [ ] MiniMax-M2.5: Comparison baseline

### Phase 5: Documentation
- [ ] Complete tutorials
- [ ] API documentation
- [ ] Best practices guide

---

## 📝 Những phần chưa rõ (cần hỏi Wi):

1. **Workflow orchestration:** 
   - Tech-lead tự động delegate hay cần human approve?
   - Có cần escalation automation không?

2. **Memory system:**
   - Dùng OpenClaw memory hay implement riêng?
   - Cross-agent knowledge sharing mechanism?

3. **Skill creation:**
   - Cần tạo skill mới hay adapt từ agent-team?
   - Priority skills nào cần implement trước?

4. **MCP Integration:**
   - Cần những MCP servers nào?
   - Context7, GitHub, Sequential Thinking - có available không?

---

## 🚀 Next Actions:

1. **Push templates lên GitHub** → wipal/oc-team-workflow-research
2. **Tạo research documentation** trong repo
3. **Implement tool profiles** trong OpenClaw config
4. **Test với 4 models**

---

*Created by Hina 🍀*