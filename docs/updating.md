# 🔄 Staying Up To Date

Codey has built-in update mechanisms to make sure you always have access to the latest features, bug fixes, and agent improvements.

---

## 💻 CLI Updates

The Codey CLI checks for updates asynchronously on startup by query checking releases on `fares-moustafa/Codey-Community` or NPM (depending on how you installed).

### Manual Upgrade/Downgrade

You can manually trigger an update or switch between specific versions using the `upgrade` command:

```bash
# Upgrade to the latest version
codey upgrade

# Upgrade or downgrade to a specific version
codey upgrade 3.5.0
```

### Configuration

You can customize the self-update behavior in your configuration file (typically located at `~/.codey/config.json`).

```json
{
  "autoupdate": "notify"
}
```

Available options for `autoupdate`:
* `true`: Automatically downloads and installs the update without prompt (Default).
* `"notify"`: Notifies you in the CLI when a new version is available but does not install it.
* `false`: Completely disables update checks.

You can also override and disable updates by setting the environment variable:
```bash
export CODEY_DISABLE_AUTOUPDATE=1
```

---

## 🖥️ Desktop App Updates

The desktop application has an integrated auto-updater powered by Tauri.
* **Update Server**: The app queries the Tauri update endpoint located at:
  `https://github.com/fares-moustafa/Codey-Community/releases/latest/download/latest.json`
* **Flow**: If a new version is declared in `latest.json`, a pop-up appears inside the desktop app offering to download and relaunch with the new version.

---

## 🛡️ Rollbacks & Troubleshooting

If a new version encounters issues, you can easily roll back to any previous release:

1. Look up previous release versions on the [GitHub Releases](https://github.com/fares-moustafa/Codey-Community/releases) page.
2. Run the pinned upgrade command:
   ```bash
   codey upgrade 3.5.0
   ```
3. If path issues occur, run the installation script again:
   ```bash
   curl -fsSL https://raw.githubusercontent.com/fares-moustafa/Codey-Community/main/install | bash -s -- --version 3.5.0
   ```
