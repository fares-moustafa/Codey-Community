# 🔗 n8n Workflows for Codey

Connecting Codey to **n8n** allows you to orchestrate external notifications, ingest issue tracker data, run scheduled audits, and sync your development environments with third-party APIs.

---

## 🏗️ Connecting Codey CLI to n8n Webhooks

You can trigger a Codey CLI execution via n8n by calling the shell node or hitting a local webhook running the CLI command.

### Example Workflow: Auto-triage GitHub Issues with Codey

```
[ GitHub Webhook: New Issue ] ───> [ HTTP Request: Call Codey Agent ] ───> [ Post Comment to GitHub ]
```

1.  **Trigger (GitHub)**: Fired whenever a user opens a new issue in your repository.
2.  **Action (HTTP Request / Execute Command)**: Trigger the local Codey CLI to draft a response:
    ```bash
    codey run --prompt "Analyze this issue: {{ $json.body }}. Suggest a fixing strategy."
    ```
3.  **Result**: Post the formulated answer as a GitHub issue comment.

---

## 📂 Community Shared Workflows

Check out the community templates directory:
*   `workflows/auto-release-notifier.json`: Post update notes to Slack/Discord when a new Tauri build finishes.
*   `workflows/daily-standup-summarizer.json`: Aggregate git commits from the last 24 hours and draft a standup update.

To share your n8n `.json` workflow exports, please open a PR adding them to the `/workflows` directory in this folder.
