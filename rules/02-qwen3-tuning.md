# 🛠️ Windows & Qwen3 Optimization
- **Paths**: Use Windows format (`\`) for all file operations.
- **Shell**: Use Powershell/CMD compatible commands (e.g., `type` instead of `cat`).
- **Precision**: Provide exact line numbers and file paths for all edits.
- **Validation**: After every edit, run `python -m py_compile <file>` or an equivalent syntax check to ensure no errors were introduced.
- **Brevity**: Output code only when requested, minimize conversational filler.
