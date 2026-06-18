# 📚 Getting Started with Codey

Welcome to Codey! This guide will walk you through setting up Codey on your machine so you can start pair-programming with your agent in minutes.

---

## 💻 Prerequisites

Make sure you have the following installed on your machine:
*   [Bun](https://bun.sh) (v1.3.5 or later) or Node.js
*   [Rust](https://www.rust-lang.org) (if compiling the desktop app from source)
*   [Git](https://git-scm.com)

---

## 📥 Installation

### Method 1: Using pre-built desktop releases
Go to the **Releases** page of this repository and download the package matching your OS:
*   **macOS**: Download the `.dmg` or build matching your architecture (Apple Silicon `aarch64` or Intel `x86_64`).
*   **Windows**: Download the `.msi` or `.exe` installer.
*   **Linux**: Download the `.deb` or `AppImage` package.

### Method 2: Running from source (Development)
If you want to run the application in development mode:

1.  Clone the repository:
    ```bash
    git clone https://github.com/fares-moustafa/Codey.git
    cd Codey
    ```
2.  Install dependencies using Bun:
    ```bash
    bun install
    ```
3.  Launch the desktop application in dev mode:
    ```bash
    bun run --cwd packages/desktop tauri dev
    ```

---

## ⚙️ Initial Configuration

Upon the first launch:
1.  **Select Your Theme**: Customize your workspace using one of our 20+ built-in visual styles (found in Settings).
2.  **API Key Setup**: Add your LLM provider api key (e.g. Gemini, OpenAI, Anthropic) under **Settings > Models**.
3.  **Open Workspace**: Click "Open Folder" and point Codey to your codebase to start editing, debugging, and planning!
