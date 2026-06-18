# 🤖 How to use WorkPilot in Codey

**WorkPilot** is Codey's state-of-the-art automation suite that lets AI agents plan, execute terminal commands, edit files, and run test suites directly in your workspace. It bridges the gap between static LLM chats and active terminal operations.

---

## 🌟 Key Features of WorkPilot

*   **Terminal Sandboxing**: Safely run shell commands (via Bun/Rust backend).
*   **Active Agent Loop**: The agent can schedule actions, evaluate command outputs, and run diagnostics without blocking your editor.
*   **Interactive Command Logs**: Track every single process spun up by the agent with real-time logs, input streams, and terminations.

---

## 🚀 Running Your First Automated Task

To trigger WorkPilot to execute or build something:

1.  **Open the Chat Interface**: Create a new session in your Codey Desktop App.
2.  **Request a Goal**: Tell the agent what you want to accomplish. For example:
    > "Create a new Solid.js component in packages/ui/src/button.tsx and verify that the package compiles."
3.  **Approve Permissions**:
    *   WorkPilot will draft an execution plan.
    *   A permission banner will prompt you when the agent requests shell command execution (e.g., `bun run build`).
    *   Click **Approve** to authorize the process or **Deny** to stop it.
4.  **Watch Live Output**: You will see a live console streaming the build process. If it fails, WorkPilot automatically reads the logs, finds the error line, and corrects the code.

---

## 🛡️ Security & Permissions

Because terminal execution can be dangerous, WorkPilot implements a local permissions framework:
*   **Command Verification**: Codey prompts you for all write operations and terminal executions.
*   **Permissions Schema**: Customize your execution safety profiles under **Settings > Developer Settings** to specify which CLI commands are automatically approved or always denied.
