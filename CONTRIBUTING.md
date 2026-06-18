# Contributing to Codey Community

Thanks for helping make Codey better! This repository is the community and distribution hub for Codey — releases, docs, issues, discussions, and shared resources (agent templates, prompts, skills, n8n workflows).

There are several ways to contribute, depending on what you want to do.

---

## 🐛 Reporting bugs

1. Search [existing issues](https://github.com/fares-moustafa/Codey-Community/issues) to avoid duplicates.
2. Open a new issue with the **Bug Report** template.
3. Include: a clear summary, exact steps to reproduce, expected vs. actual behavior, your OS + Codey version (`codey --version`), and logs/screenshots if you have them.

## 💡 Requesting features

Open an issue with the **Feature Request** template, or start a thread in [Discussions → Ideas](https://github.com/fares-moustafa/Codey-Community/discussions). Describe the problem first, then your proposed solution and any alternatives.

## 💬 Asking questions

Use [Discussions → Q&A](https://github.com/fares-moustafa/Codey-Community/discussions) rather than issues for usage questions. See [SUPPORT.md](./SUPPORT.md) for all support channels.

---

## 📦 Contributing to this repository

This repo hosts documentation and community resources. You can contribute to:

- **`docs/`** — guides and references.
- **`contributions/`** — agent templates, prompts, skills, and n8n workflows.
- **`ROADMAP.md`** — corrections and suggestions (via issue/PR).

### Workflow

1. **Fork** this repository.
2. **Create a branch** named for your change:
   ```bash
   git checkout -b docs/improve-getting-started
   # or: feature/new-agent-template, fix/typo-in-readme
   ```
3. **Make your changes.** Keep Markdown clean and consistent with the existing style.
4. **Test links and code blocks.** Make sure commands actually work and internal links resolve.
5. **Commit** with a clear message:
   ```bash
   git commit -m "docs: clarify musl install steps"
   ```
6. **Open a Pull Request** against `main` using the PR template. Describe what changed and why.

### Sharing an agent template, prompt, or skill

Add it to the matching file under `contributions/`:

- Agent definitions → [`contributions/agent-templates.md`](./contributions/agent-templates.md)
- Prompts & skills → [`contributions/prompts-and-skills.md`](./contributions/prompts-and-skills.md)
- n8n workflows → [`contributions/n8n-workflows.md`](./contributions/n8n-workflows.md)

Each entry should include a short description, the config/code, and (optionally) your handle for credit.

---

## ✅ Pull request checklist

- [ ] The change is focused and described clearly.
- [ ] Markdown renders correctly (headings, code fences, tables).
- [ ] Commands and config examples are tested and use the correct names (`codey`, not legacy names).
- [ ] Internal links resolve.
- [ ] You agree to license your contribution under the repository's [MIT License](./LICENSE).

---

## 📜 Code of Conduct

By participating, you agree to uphold our [Code of Conduct](./CODE_OF_CONDUCT.md). Be respectful, constructive, and welcoming.

---

## 🔐 Reporting security issues

**Do not** open a public issue for security vulnerabilities. Follow the [Security Policy](./SECURITY.md) instead.

---

Thank you for contributing! 🙌
