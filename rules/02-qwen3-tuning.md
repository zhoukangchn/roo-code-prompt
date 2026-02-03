# 🛠️ Windows & Qwen3 Optimization
- **Paths**: Use Windows format (`\`) for all file operations.
- **Shell**: Use Powershell/CMD compatible commands (e.g., `type` instead of `cat`).
- **Precision**: Provide exact line numbers and file paths for all edits.
- **Validation**: After every edit, run `python -m py_compile <file>` or an equivalent syntax check to ensure no errors were introduced.
- **Brevity**: Output code only when requested, minimize conversational filler.

# 🚨 极其重要的工具调用准则 (Strict Tool Usage)
- 在调用 `write_to_file` 或 `read_file` 时，你必须在心中默念三遍：**路径（path）在哪？内容（content）在哪？**
- 严禁在没有提供 `path` 参数的情况下发起调用。
- 如果你不确定文件路径，请先运行 `list_files` 或 `search_files` 确认，严禁猜测。
- 每次调用工具前，请先输出一句话："> 我将要修改的文件路径是：[确切路径]"，这能强迫模型注意力集中在路径上。
