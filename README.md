# Roo Code Prompt v2: Agentic Engineering Patterns 🦞
# 适用于 Roo Code (Cline) + Qwen3 / Claude / Gemini

这是一套基于社区最佳实践（Cline Rules / Agentic Workflow）优化的 Prompt 模板库。

---

## 🚀 Quick Start (Windows)
1. **Clone**: `git clone git@github.com:zhoukangchn/roo-code-prompt.git %USERPROFILE%\roo-code-prompt`
2. **Configure**: Create a `.clinerules` file in your project root using the template in `AGENTS.md`.
3. **Run**: Start Roo Code and ask: *"Read my global rules and start Architect mode."*

---

## 🚀 核心原则 (Rules of Engagement)
在使用 Roo Code 时，建议先在 **Custom Instructions** 中加入以下全局规则：
1. **先思考后行动**：在修改文件前，先列出你的分析和执行计划。
2. **最小侵入性**：除非明确要求，否则不要删除代码注释，不要改动不相关的逻辑。
3. **闭环验证**：完成修改后，必须主动尝试运行测试或检查语法。
4. **Git 规范**：每次功能点完成后，主动提示用户进行提交。

---

## 🛠️ 任务专精模板

### 1. 架构师模式 (Architect Mode)
**适用场景**：新功能设计、复杂逻辑梳理。
```markdown
Act as a Senior Software Architect. 
Task: {design_task}

Please follow this workflow:
1. **Explore**: Scan the current project structure and list the most relevant files.
2. **Design**: Create a technical design plan. Use Mermaid diagrams if complex.
3. **Impact**: Identify which existing modules will be affected.
4. **Approval**: Wait for my confirmation before editing any files.
```

### 2. 开发者模式 (Developer Mode - Test Driven)
**适用场景**：实现具体功能，要求高代码质量。
```markdown
Act as a Senior Full-stack Developer.
Goal: {feature_request}

Constraint:
- Use Test-Driven Development (TDD) approach.
- Step 1: Write a failing test case in `tests/`.
- Step 2: Implement the minimal code to pass the test.
- Step 3: Refactor for performance and readability.
- Step 4: Verify the fix with `pytest` or `npm test`.
```

### 3. 调试专家模式 (Debug Mode)
**适用场景**：排查报错、解决逻辑 Bug。
```markdown
Act as a Debugging Specialist. 
Issue: {error_description}

Instructions:
1. **Trace**: Search the logs and use `grep` to find where this error originates.
2. **Analyze**: Explain WHY this error is happening (Root Cause).
3. **Hypothesize**: Propose 2-3 potential fixes.
4. **Verify**: Apply the best fix and run the code to ensure the error is gone.
```

### 4. 代码重构模式 (Refactor Mode)
**适用场景**：消除技术债、优化陈旧代码。
```markdown
Task: Refactor {module_name} to improve maintainability.

Principles:
- Single Responsibility Principle (SRP).
- DRY (Don't Repeat Yourself).
- Add type hints (Python 3.10+).
- Ensure function length stays under 30 lines.
- NO functional changes allowed unless bug discovered.
```

### 5. 极简“苦力”模式 (The Exec Mode)
**适用场景**：公司 Qwen3 模型能力有限时，通过极度拆解任务来换取成功率。
```markdown
Role: Precise Code Executor.
Input Code: {code_snippet}
Target File: {file_path}

Task:
1. Replace lines {start_line} to {end_line} with the Input Code provided.
2. Maintain existing indentation perfectly.
3. Run `python -m py_compile {file_path}` to check for syntax errors.
```

---

## 💡 给 Qwen3 的特别调优建议
如果 Qwen3 表现不稳定，请在 Prompt 结尾追加：
- "Think step by step."
- "Output code only, no conversational filler."
- "Verify the file content with `cat` after editing to ensure integrity."

---
*Generated with ❤️ by 阿龙 (LobsterAhLong) via OpenClaw*
