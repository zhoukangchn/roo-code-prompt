# AGENTS.md - Prompt Engineering & Library Rules

This file defines how Agents (including Ah Long and Roo Code) should interact with this repository and the prompts within it.

## 🦞 The Librarian's Code
When updating or adding new prompts to this library, follow these mandates:

1. **Precision First**: Prompts must be unambiguous. Qwen3 requires clear constraints and step-by-step instructions.
2. **Context Injection**: Use `{placeholder}` tags for dynamic content.
3. **Closed-Loop Feedback**: Every "Action" prompt must include a "Verification" step (e.g., "Run tests" or "Check syntax").
4. **Model Specificity**: If a prompt is specifically tuned for Qwen3's quirks (like the "The Exec" mode), document it clearly.

## 🛠️ Usage Patterns for Roo Code (at Work)
To get the most out of this library while on the company machine:

### 1. The Reference Pattern (Universal)
Before starting a complex task, tell Roo Code:
> "Read the `Architect Mode` template from `README.md` in my `roo-code-prompt` repo and apply its logic to my current task."

### 2. The .clinerules Setup (Recommended for Windows/macOS/Linux)
Create a `.clinerules` file in your **Business Repo** root.

**For Windows Users:**
```markdown
# 📚 Loading Knowledge
Before editing files, you MUST read the global rules:
%USERPROFILE%\roo-code-prompt\AGENTS.md
%USERPROFILE%\roo-code-prompt\README.md

# 🛠️ Windows/Qwen3 Directives
- Use Windows path format (\).
- Use Powershell/CMD compatible commands (e.g., `type` instead of `cat`).
- Follow the 'Plan -> Execute -> Verify' workflow.
```

### 3. The Custom Instructions (Global Boost)
Copy this into Roo Code's **Custom Instructions** settings:
```markdown
- Always analyze project structure before suggesting changes.
- Refer to `AGENTS.md` in the `roo-code-prompt` directory for core behaviors.
- For Qwen3: Be explicit with file paths and line numbers.
- Always check for syntax errors after editing a file.
```

## 🔄 Library Maintenance Workflow
1. **Identify Gap**: When a prompt fails to produce good results with Qwen3, note the failure.
2. **Refine**: Update the template in `README.md` or create a new specialist mode.
3. **Commit**: Use descriptive commit messages (e.g., `fix: optimize refactor mode for qwen3 logic`).
4. **Sync**: Push to GitHub so the company machine can pull the latest "brain" updates.

---
*Managed by 阿龙 (LobsterAhLong) | Powered by OpenClaw*
