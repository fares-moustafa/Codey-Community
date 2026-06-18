# ⚙️ How to Configure Codey Agents

You can customize how Codey agents behave, their system prompts, and which tools they have access to. This guide covers writing custom agent configuration schemas.

---

## 🛠️ Custom Agent Configuration

Codey reads agent definitions from an `agents.json` configuration file located at the root of your workspace, or globally under your application settings folder.

### Configuration Schema Example (`agents.json`)

Create an `agents.json` at the root of your project:

```json
{
  "agents": [
    {
      "id": "frontend-expert",
      "name": "Senior Frontend Architect",
      "systemPrompt": "You are a senior frontend developer specializing in React, SolidJS, and CSS. Reject generic designs and enforce visual excellence and minimalism.",
      "allowedTools": [
        "view_file",
        "replace_file_content",
        "multi_replace_file_content",
        "write_to_file"
      ],
      "model": "gemini-2.5-pro"
    },
    {
      "id": "backend-tester",
      "name": "QA & Test Runner",
      "systemPrompt": "You are an automated test runner. Your main task is to execute tests, parse test failures, and write test suites using Jest or Vitest.",
      "allowedTools": [
        "run_command",
        "view_file"
      ],
      "model": "gemini-2.5-flash"
    }
  ]
}
```

---

## 🔑 Customizing System Prompts

You can write specialized system instructions in markdown or plain text files and reference them in the settings page. This allows you to enforce codebase conventions (e.g., "Always use Tailwind CSS", "Maintain strict TypeScript typings").

### Guidelines for Effective System Prompts:
1.  **Define Role & Background**: Tell the agent exactly what role they have (e.g., "Senior Rails Developer").
2.  **Coding Standards**: Specify library rules (e.g., "Use Solid-JS catalog variables").
3.  **Prohibitions**: Add strict restrictions (e.g., "Do not create new packages without permission").
