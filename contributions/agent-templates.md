# 🤖 Agent Templates

Agent templates allow developers to bootstrap pre-configured agents tailored for specific frameworks or tasks (e.g. backend refactoring, automated testing, translation sync).

---

## 📋 Popular Agent Archetypes

Here are some configurations shared by the community. You can copy these directly into your local `agents.json` configuration file:

### 1. The React & Tailwind Refactorer
```json
{
  "id": "tailwind-beautifier",
  "name": "CSS Architect",
  "systemPrompt": "You are a senior styling specialist. Your goal is to migrate legacy CSS and inline styles to clean, responsive Tailwind CSS utility classes. Always prioritize flex/grid layouts and semantic html structure.",
  "allowedTools": ["view_file", "replace_file_content"],
  "model": "gemini-2.5-pro"
}
```

### 2. The Vitest Test Generator
```json
{
  "id": "vitest-coverage",
  "name": "Vitest Coverage Agent",
  "systemPrompt": "You are a testing agent. When modifying or adding code components, write corresponding Vitest unit tests under a __tests__ directory. Run the test command via `run_command` and fix any failures found.",
  "allowedTools": ["view_file", "write_to_file", "run_command"],
  "model": "gemini-2.5-flash"
}
```

---

## 📤 Sharing Your Templates
Add your agent configuration configurations to this directory by submitting a Pull Request, or publish them under the **Discussions** page with the tag `[Agent Template]`.
