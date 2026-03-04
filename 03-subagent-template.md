# 🤖 Subagent Template

## Agent Information

| Field | Value |
|-------|-------|
| **Agent ID** | [agent-id] |
| **Agent Name** | [Tên agent] |
| **Created Date** | [YYYY-MM-DD] |
| **Version** | 1.0 |

---

## 1. Purpose & Scope

### Purpose
[Mục đích chính của agent này]

### Scope
**In Scope:**
- [Task type 1]
- [Task type 2]

**Out of Scope:**
- [Task không làm]

---

## 2. Model Configuration

### Primary Model
```yaml
provider: [bailian/zai/openrouter]
model: [model-name]
thinking: [off/low/medium/high]
```

### Fallback Chain
```yaml
fallbacks:
  - provider: [provider]
    model: [model-name]
  - provider: [provider]
    model: [model-name]
```

### Model Selection Reason
[Tại sao chọn model này? Cost/Speed/Quality balance]

---

## 3. Capabilities

### Core Capabilities
| Capability | Level | Notes |
|------------|-------|-------|
| [Capability 1] | Strong/Medium/Basic | |
| [Capability 2] | | |

### What This Agent Excels At
- [Strength 1]
- [Strength 2]

### Known Limitations
- [Limitation 1]
- [Limitation 2]

---

## 4. Tools & Permissions

### Available Tools
```yaml
tools:
  allow:
    - read
    - write
    - exec
    - web_search
    - web_fetch
    # Add more as needed
```

### Exec Permissions
```yaml
exec:
  security: [deny/allowlist/full]
  host: [sandbox/gateway/node]
  # If allowlist:
  allowlist:
    - git
    - npm
    - docker
```

### File Access
```yaml
workspace:
  - /data/workspace/
  - [Custom paths]
```

---

## 5. Agent Configuration

### Full Config Example
```json
{
  "id": "agent-id",
  "model": {
    "primary": "provider/model-name",
    "fallbacks": ["provider/model-2"]
  },
  "thinking": "medium",
  "tools": {
    "profile": "coding",
    "allow": ["read", "write", "exec"]
  },
  "subagents": {
    "allowAgents": ["other-agent-id"]
  }
}
```

### Skills (Optional)
```yaml
skills:
  - skill-name-1
  - skill-name-2
```

---

## 6. Prompting Guidelines

### System Prompt Framework
```
You are [Agent Name], a [role description].

Your primary responsibilities:
- [Responsibility 1]
- [Responsibility 2]

You excel at [strengths].

When you encounter [situation], you should [action].

Always [important rule].
Never [prohibited action].
```

### Example Prompts

**Prompt 1: [Task Type]**
```
[User prompt example]
```

**Expected Output:**
```
[Expected agent response]
```

---

## 7. Task Routing

### When to Use This Agent
- [Condition 1]
- [Condition 2]
- [Keyword triggers]: [list keywords]

### Keywords/Triggers
```yaml
triggers:
  - fix
  - code
  - debug
  - docker
  - [more keywords]
```

---

## 8. Performance Metrics

### Success Metrics
| Metric | Target | Current |
|--------|--------|---------|
| Response Time | < 5s | |
| Success Rate | > 95% | |
| User Satisfaction | > 4.5/5 | |

### Monitoring
```yaml
monitoring:
  - response_time
  - token_usage
  - error_rate
  - fallback_rate
```

---

## 9. Testing Checklist

### Pre-Deployment Tests
- [ ] Basic chat test passed
- [ ] Tool access verified
- [ ] Fallback chain working
- [ ] Edge cases handled
- [ ] Permission boundaries tested

### Test Cases

| Test Case | Input | Expected Output | Status |
|-----------|-------|-----------------|--------|
| Basic chat | "Hi" | Friendly greeting | ⏳ |
| [Task type] | [Input] | [Output] | ⏳ |

---

## 10. Maintenance

### Update Schedule
- **Review:** Monthly
- **Update:** As needed
- **Owner:** [Who maintains]

### Known Issues
| Issue | Status | Workaround |
|-------|--------|------------|
| [Issue 1] | Open/Fixed | [Workaround] |

---

## 11. Cost Considerations

### Expected Costs
```
Average tokens per request: [X]
Cost per 1K tokens: $[Y]
Expected daily requests: [Z]
Estimated daily cost: $[Total]
```

### Cost Optimization
- [Optimization tip 1]
- [Optimization tip 2]

---

## 12. Integration

### With Other Agents
```yaml
collaborates_with:
  - agent-id-1
  - agent-id-2
```

### Handoff Protocol
```
When [condition], hand off to [agent-id]:
- Provide context: [what context]
- Format: [format]
```

---

*Template by Hina 🍀*