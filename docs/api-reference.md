# 🔌 API & MCP Tool Reference

Codey leverages the **Model Context Protocol (MCP)** to allow external services, local packages, and tools to connect directly to the model.

---

## 🛠️ Model Context Protocol (MCP) Integration

Codey can dynamically load tools from MCP servers. This reference describes how tool calls are structured and executed.

### Core Tools Available in Codey

| Tool Name | Action Description | Target Arguments |
| :--- | :--- | :--- |
| `view_file` | Read files (text/binary) from workspace. | `AbsolutePath`, `StartLine`, `EndLine` |
| `write_to_file` | Create or overwrite files in workspace. | `TargetFile`, `CodeContent`, `Overwrite` |
| `replace_file_content` | Apply contiguous edits to a file. | `TargetFile`, `TargetContent`, `ReplacementContent` |
| `run_command` | Execute shell commands in terminal. | `CommandLine`, `Cwd`, `WaitMsBeforeAsync` |
| `grep_search` | Search files using Ripgrep patterns. | `Query`, `SearchPath`, `IsRegex` |

---

## 🔄 Tauri v2 Updater Protocol Reference

Codey Desktop handles updates using the Tauri v2 updater plugin. For self-hosting releases, you must serve a JSON manifest complying with the following schema:

### `latest.json` Schema

```json
{
  "version": "3.5.1",
  "notes": "Premium theme additions and cleaner sidebar layout defaults.",
  "pub_date": "2026-06-18T14:00:00Z",
  "platforms": {
    "darwin-aarch64": {
      "signature": "dW50cnVzdGVkIGNvbW1lbnQ6...",
      "url": "https://github.com/fares-moustafa/Codey/releases/download/v3.5.1/Codey-desktop-macos-aarch64.tar.gz"
    },
    "windows-x86_64": {
      "signature": "dW50cnVzdGVkIGNvbW1lbnQ6...",
      "url": "https://github.com/fares-moustafa/Codey/releases/download/v3.5.1/Codey-desktop-windows-x86_64.msi.zip"
    },
    "linux-x86_64": {
      "signature": "dW50cnVzdGVkIGNvbW1lbnQ6...",
      "url": "https://github.com/fares-moustafa/Codey/releases/download/v3.5.1/Codey-desktop-linux-x86_64.AppImage.tar.gz"
    }
  }
}
```

*Note: Signatures are generated using `tauri-cli` or `minisign` during the build process.*
