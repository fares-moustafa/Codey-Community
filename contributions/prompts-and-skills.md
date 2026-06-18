# 🧩 Community Prompts & Skills

Help grow the Codey ecosystem by sharing your custom prompts and skills! Skills allow agents to perform complex, repository-specific tasks (e.g. data quality checks, custom formatting, build scripts) with specialized rules.

---

## 🛠️ What is a Codey Skill?

A **Skill** is a folder located in your configuration directory (`~/.codey/skills/`) containing:
1.  **`SKILL.md`**: Main instruction set in markdown with YAML frontmatter defining its scope and activation criteria.
2.  **`manifest.json`**: Definition file specifying the metadata, version, and dependencies.
3.  **`scripts/`** (Optional): Shell, Node, or Python scripts called by the skill instructions.

---

## 📝 Submitting a Skill Template

When sharing your skill with the community, structure it as follows:

```yaml
---
name: my-awesome-skill
description: Activates when doing X to help automate Y.
---
# Instructions
1. First, analyze the codebase for pattern Z.
2. Run script `scripts/analyze.sh` to check for details.
3. Perform repairs using `replace_file_content`.
```

### 📤 How to share:
Open a Pull Request or create a discussion post in the **Discussions** section with the category **🧩 Show & Tell** and use the title prefix `[Skill] Name of Skill`.
