# Roo Code Prompt v2: Agentic Engineering Patterns 🦞
# 适用于 Roo Code (Cline) + Qwen3 / Claude / Gemini

这是一套基于社区最佳实践（Roo Rules / Agentic Workflow）优化的 Prompt 模板库。

---

## 🚀 Quick Start (Windows)
1. **Clone**: `git clone git@github.com:zhoukangchn/roo-code-prompt.git %USERPROFILE%\roo-code-prompt`
2. **Configure**: 
   - Create a directory named `.roo/rules/` in your **Business project root**.
   - Copy all files from the `rules/` directory in this repo into that folder.
3. **Run**: Start Roo Code and ask: *"Read my global rules and start Architect mode."*

---

## 📂 Modular Rules Structure
We recommend using the `.roo/rules/` directory for modular rule management:
- `01-core.md`: Core identity and link to this library.
- `02-qwen3-tuning.md`: Specific fixes for Qwen3 and Windows quirks.
- `03-modes.md`: Index for specialized task modes.

---

## 🚀 核心原则 (Rules of Engagement)
在使用 Roo Code 时，建议先在 **Custom Instructions** 中加入以下全局规则：
1. **先思考后行动**：在修改文件前，先列出你的分析和执行计划。
2. **最小侵入性**：除非明确要求，否则不要删除代码注释，不要改动不相关的逻辑。
3. **闭环验证**：完成修改后，必须主动尝试运行测试或检查语法。
4. **Git 规范**：每次功能点完成后，主动提示用户进行提交。
5. **加载优先级**：Roo Code 会按以下顺序寻找规则：
   - `.roo/rules/` 目录下的 `.md` 文件 (现代推荐做法)
   - 根目录下的 `.roorules` 文件
   - 根目录下的 `AGENTS.md` 文件 (核心准则)

---

## 🛠️ 任务专精模板 (Specialist Modes)
Refer to individual sections in this file for detailed prompt templates:
- **Architect Mode**
- **Developer Mode**
- **Debug Mode**
- **Refactor Mode**
- **The Exec Mode** (Optimized for Qwen3)

---
*Generated with ❤️ by 阿龙 (LobsterAhLong) via OpenClaw*
