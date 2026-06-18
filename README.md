<div align="center">

# Codey Community

**The home for Codey releases, updates, and the developer community.**

[![Latest Release](https://img.shields.io/github/v/release/fares-moustafa/Codey-Community?label=latest&color=orange)](https://github.com/fares-moustafa/Codey-Community/releases/latest)
[![Downloads](https://img.shields.io/github/downloads/fares-moustafa/Codey-Community/total?color=orange)](https://github.com/fares-moustafa/Codey-Community/releases)
[![License: MIT](https://img.shields.io/badge/License-MIT-orange.svg)](./LICENSE)
[![Issues](https://img.shields.io/github/issues/fares-moustafa/Codey-Community?color=orange)](https://github.com/fares-moustafa/Codey-Community/issues)
[![Discussions](https://img.shields.io/github/discussions/fares-moustafa/Codey-Community?color=orange)](https://github.com/fares-moustafa/Codey-Community/discussions)

[Install](#-installation) · [Update](#-staying-up-to-date) · [Docs](./docs) · [Roadmap](./ROADMAP.md) · [Contribute](./CONTRIBUTING.md) · [العربية](./README.ar.md)

</div>

---

## 🤖 What is Codey?

**Codey** is an AI coding agent built for the terminal — a fast, keyboard-first TUI plus a cross-platform desktop app. It pairs with you to read, write, and refactor code, run commands, drive test suites, and orchestrate multi-step tasks through the **Model Context Protocol (MCP)**.

This repository — **Codey Community** — is the public hub for the project. It hosts:

- 📦 **Releases** — every Codey version (CLI binaries + desktop installers) is published here.
- 🔄 **Updates** — the CLI self-updater and the desktop auto-updater both check this repo.
- 🐛 **Issues & feedback** — bug reports and feature requests.
- 💬 **Discussions** — Q&A, show & tell, and ideas.
- 📚 **Docs & contributions** — guides, agent templates, prompts, skills, and n8n workflows.

> The Codey application source lives in a separate repository. This repo is the **distribution and community** front door.

---

## 📥 Installation

### Quick install (macOS / Linux / WSL)

```bash
curl -fsSL https://raw.githubusercontent.com/fares-moustafa/Codey-Community/main/install | bash
```

Install a specific version:

```bash
curl -fsSL https://raw.githubusercontent.com/fares-moustafa/Codey-Community/main/install | bash -s -- --version 3.5.1
```

### Package managers

```bash
# npm
npm install -g codey

# bun
bun install -g codey

# yarn
yarn global add codey

# Homebrew (tap)
brew install fares-moustafa/tap/codey
```

### Pre-built releases (desktop app)

Grab the installer for your platform from the [**Releases**](https://github.com/fares-moustafa/Codey-Community/releases/latest) page:

| Platform | Asset |
| :--- | :--- |
| **macOS** (Apple Silicon) | `Codey-desktop-darwin-aarch64.dmg` |
| **macOS** (Intel) | `Codey-desktop-darwin-x86_64.dmg` |
| **Windows** | `Codey-desktop-windows-x86_64-setup.exe` |
| **Linux** | `Codey-desktop-linux-x86_64.AppImage` |

CLI archives are also attached to each release as `codey-<os>-<arch>.zip` (or `.tar.gz` on Linux).

See [**docs/installation.md**](./docs/installation.md) for every method, including musl/baseline builds and offline binaries.

---

## 🔄 Staying up to date

Codey keeps itself current — you rarely have to think about it.

- **CLI self-update** — on launch, Codey checks this repo (or npm / Homebrew, depending on how you installed) for a newer version and can upgrade automatically.
- **Desktop auto-update** — the desktop app uses the Tauri updater pointed at this repo's `latest.json`.
- **Manual upgrade** — run:

  ```bash
  codey upgrade            # upgrade to the latest version
  codey upgrade 3.5.1      # upgrade/downgrade to a specific version
  ```

Update behavior is configurable (`autoupdate`: `true` | `"notify"` | `false`) and a failed upgrade can be rolled back. Full details in [**docs/updating.md**](./docs/updating.md).

---

## 📚 Documentation

| Guide | What's inside |
| :--- | :--- |
| [Getting Started](./docs/getting-started.md) | Prerequisites, first run, first task |
| [Installation](./docs/installation.md) | Every install method in detail |
| [Updating](./docs/updating.md) | Channels, self-update, `codey upgrade`, rollback |
| [Release Process](./docs/release-process.md) | How releases flow into this repo |
| [Configure Agents](./docs/configure-agents.md) | Custom agents, prompts, tool scopes |
| [WorkPilot Guide](./docs/workpilot-guide.md) | The terminal automation suite |
| [API & MCP Reference](./docs/api-reference.md) | Tools, MCP, and the updater protocol |

---

## 🧩 Community contributions

Share what you build and use what others have shared:

- 🤖 [Agent templates](./contributions/agent-templates.md)
- 🧩 [Prompts & skills](./contributions/prompts-and-skills.md)
- 🔗 [n8n workflows](./contributions/n8n-workflows.md)

Browse the [contributions index](./contributions/README.md) or add your own via a pull request.

---

## 🗺️ Roadmap

See what's shipping next on the [**public roadmap**](./ROADMAP.md). Want to influence it? Open a [discussion](https://github.com/fares-moustafa/Codey-Community/discussions) or a [feature request](https://github.com/fares-moustafa/Codey-Community/issues/new/choose).

---

## 🤝 Contributing & support

- 🐛 Found a bug? [Open an issue](https://github.com/fares-moustafa/Codey-Community/issues/new/choose).
- 💡 Have an idea? Start a [discussion](https://github.com/fares-moustafa/Codey-Community/discussions).
- 📖 Want to contribute? Read the [Contributing Guide](./CONTRIBUTING.md).
- ❓ Need help? See [Support](./SUPPORT.md).

Please follow our [Code of Conduct](./CODE_OF_CONDUCT.md). Security issues? See our [Security Policy](./SECURITY.md).

---

## 📄 License

Codey Community is released under the [MIT License](./LICENSE).

<div align="center">
<sub>Built with ❤️ by Fares Moustafa and the Codey community.</sub>
</div>
