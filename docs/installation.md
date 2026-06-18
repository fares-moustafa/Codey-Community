# 📥 Codey Installation Guide

This guide details all available methods to install, build, and configure the **Codey CLI** and **Desktop App**.

---

## ⚡ Quick Install (macOS / Linux / WSL)

The fastest way to install the Codey CLI is via our unified bash install script. It automatically detects your operating system, CPU architecture, glibc/musl compatibility, and AVX2 support.

Run the following command in your terminal:

```bash
curl -fsSL https://raw.githubusercontent.com/fares-moustafa/Codey-Community/main/install | bash
```

### Install Script Options

You can customize the installation by downloading the script and running it with options, or passing arguments through stdin:

| Option | Description |
| :--- | :--- |
| `-v, --version <version>` | Install a specific version (e.g. `3.5.1`) |
| `-b, --binary <path>` | Install directly from a local binary path instead of downloading |
| `--no-modify-path` | Prevent the installer from adding Codey to your shell configuration files |

**Examples:**

```bash
# Install specific version (3.5.1)
curl -fsSL https://raw.githubusercontent.com/fares-moustafa/Codey-Community/main/install | bash -s -- --version 3.5.1

# Run local installer with no path modification
./install --no-modify-path
```

The script installs the binary to `~/.codey/bin/codey` and modifies your shell config (`.zshrc`, `.bashrc`, `.profile`, or `config.fish`) to append it to your `$PATH`.

---

## 📦 Package Managers

Codey is published on registries for easy global installations.

### NPM / Bun / Yarn
```bash
# npm
npm install -g codey

# bun
bun install -g codey

# yarn
yarn global add codey
```

### Homebrew (macOS / Linux)
You can tap the official repository and install via Homebrew:
```bash
brew tap fares-moustafa/tap
brew install codey
```

---

## 🖥️ Pre-built Desktop Installer

For a visual interface, download platform-specific package installers from the [**Releases Page**](https://github.com/fares-moustafa/Codey-Community/releases).

| Platform | Format | Filename |
| :--- | :--- | :--- |
| **macOS** (Apple Silicon) | DMG Installer | `Codey-desktop-darwin-aarch64.dmg` |
| **macOS** (Intel) | DMG Installer | `Codey-desktop-darwin-x86_64.dmg` |
| **Windows** | Setup Executable | `Codey-desktop-windows-x86_64-setup.exe` |
| **Linux** | AppImage | `Codey-desktop-linux-x86_64.AppImage` |

---

## 🏗️ Hardware & Environment Compatibility

Our install script automatically handles specific hardware environments:

1. **glibc vs musl (Linux)**: The installer detects if your Linux system uses `musl` (e.g., Alpine Linux) or `glibc` and fetches `codey-linux-x64-musl` or `codey-linux-arm64-musl` appropriately.
2. **AVX2 Support**: For systems lacking AVX2 instructions (older Intel/AMD chips), the installer downloads the baseline binary target (`codey-linux-x64-baseline` or `codey-darwin-x64-baseline`) to prevent instruction crashes.
