# Contributing to agent-skills

Thank you for your interest in contributing! 🎉  
agent-skills is a community-driven project, and every contribution — big or small — helps make agent development better for everyone.

Please take a few minutes to read these guidelines before submitting anything.

---

## Table of Contents

- [Code of Conduct](#code-of-conduct)
- [Ways to Contribute](#ways-to-contribute)
- [Getting Started](#getting-started)
- [Adding a New Skill](#adding-a-new-skill)
- [Improving an Existing Skill](#improving-an-existing-skill)
- [Submitting Examples](#submitting-examples)
- [Pull Request Guidelines](#pull-request-guidelines)
- [Commit Message Guidelines](#commit-message-guidelines)
- [Reporting Issues](#reporting-issues)
- [Review Process](#review-process)
- [Style & Quality Standards](#style--quality-standards)

---

## Code of Conduct

By participating in this project, you agree to maintain a respectful, inclusive, and collaborative environment. We expect all contributors to:

- Be kind and constructive in all interactions
- Respect differing viewpoints and experiences
- Gracefully accept feedback
- Focus on what is best for the community

Harassment, discrimination, or disrespectful behavior of any kind will not be tolerated.

---

## Ways to Contribute

There are several ways you can contribute to this repository:

| Type | Description |
|------|-------------|
| 🆕 New Skill | Add a skill for a use case not yet covered |
| ✏️ Improve a Skill | Refine descriptions, fix errors, or improve instructions |
| 💡 Add Examples | Share example agents or workflows using existing skills |
| 🐛 Report a Bug | Open an issue if a skill behaves incorrectly or is poorly documented |
| 📖 Improve Docs | Fix typos, improve clarity, or update outdated information |
| 💬 Give Feedback | Open a discussion or comment on open issues |

---

## Getting Started

1. **Fork** this repository to your own GitHub account.
2. **Clone** your fork locally:
   ```bash
   git clone https://github.com/harishrajora/agent-skills
   cd agent-skills
   ```
3. **Create a new branch** for your contribution:
   ```bash
   git checkout -b feat/your-skill-name
   ```
4. Make your changes following the guidelines below.
5. **Push** to your fork and open a **Pull Request**.

---

## Adding a New Skill

Skills are the core of this repository. To add a new skill:

### 1. Choose the right category

Place your skill under the most relevant subdirectory inside `skills/`:

```
skills/
├── api/
├── file-handling/
├── data-processing/
└── <new-category>/    ← create one if none fits
```

If no existing category fits, you may propose a new one in your PR description.

### 2. Create the skill directory

```
skills/<category>/<your-skill-name>/
├── SKILL.md          # Required
└── examples/         # Optional but encouraged
    └── example.md
```

### 3. Write the SKILL.md

Every skill **must** have a `SKILL.md` file. Use the following template:

```markdown
---
name: your-skill-name
description: One sentence explaining what this skill does and when to use it.
---

## Overview

A brief explanation of the skill's purpose and the problem it solves.

## When to Use

List the scenarios, trigger keywords, or conditions under which an agent should invoke this skill.

- Trigger condition 1
- Trigger condition 2
- Example phrases: "do X", "help me with Y", "generate Z"

## Instructions

Step-by-step guidance for the agent when this skill is active.

1. Step one
2. Step two
3. Step three

## Examples

Optional: show one or two brief examples of inputs and expected outputs.

## Notes

Any caveats, limitations, or important considerations.
```

### 4. Checklist before submitting

- [ ] `SKILL.md` follows the template above
- [ ] The skill name is lowercase and hyphen-separated (e.g., `api-spec-generator`)
- [ ] The description is clear and concise (1–2 sentences)
- [ ] Trigger conditions are specific and actionable
- [ ] Instructions are written from the agent's perspective
- [ ] No sensitive data, credentials, or hardcoded secrets are included

---

## Improving an Existing Skill

If you find a skill that is incorrect, unclear, or outdated:

1. Open an **issue** first if the change is significant, so it can be discussed.
2. For minor fixes (typos, grammar, formatting), you can go directly to a PR.
3. Make sure your changes preserve the original intent of the skill.
4. Note what you changed and why in the PR description.

---

## Submitting Examples

Examples help the community understand how to use skills in real agent workflows. To add an example:

1. Place it in the `examples/` folder inside the relevant skill directory.
2. Name the file descriptively: `use-case-name.md` or `use-case-name.json`.
3. Include a short explanation of the scenario, the agent setup, and the expected behavior.

You can also add general examples to the top-level `examples/` directory if they demonstrate multiple skills working together.

---

## Improving Installer

You can also provide your contribution in the installer file. However, be cautious, as it is a bash file that interacts with the terminal.

---

## Pull Request Guidelines

- **One PR per skill or fix** — keep PRs focused and easy to review.
- **Write a clear PR title**, e.g.:  
  `feat: add openapi-spec-generator skill`  
  `fix: improve trigger conditions for pdf skill`  
  `docs: fix typo in xlsx SKILL.md`
- **Fill out the PR description** — explain what you added, changed, or fixed, and why.
- **Link related issues** using `Closes #issue-number` if applicable.
- **Do not include unrelated changes** in the same PR.

---

## Commit Message Guidelines

Use clear, conventional commit messages:

```
<type>: <short description>
```

| Type | When to use |
|------|-------------|
| `feat` | Adding a new skill or feature |
| `fix` | Fixing a bug or incorrect instruction |
| `docs` | Documentation-only changes |
| `refactor` | Restructuring without changing behavior |
| `chore` | Maintenance tasks (renaming, moving files) |

**Examples:**
```
feat: add selenium-automation skill
fix: correct trigger conditions in file-reading skill
docs: update CONTRIBUTING.md with example template
```

---

## Reporting Issues

If you find a problem with an existing skill or have a suggestion:

1. Check if an issue already exists before opening a new one.
2. Use a descriptive title.
3. Include:
   - The skill name and file path
   - What you expected vs. what actually happened
   - Any relevant context or examples
4. Label your issue appropriately (e.g., `bug`, `enhancement`, `question`).

---

## Review Process

All contributions go through a review before being merged:

1. A maintainer will review your PR within a reasonable timeframe.
2. You may be asked to make changes — this is normal and constructive.
3. Once approved, your PR will be merged into the `main` branch.
4. Your contribution will be credited in the repository.

We aim to be responsive and respectful throughout the review process.

---

## Style & Quality Standards

To keep the repository consistent and high quality:

- **Language**: All content must be in English.
- **Tone**: Write instructions clearly, concisely, and from the agent's perspective.
- **Formatting**: Use standard Markdown. Avoid raw HTML unless necessary.
- **File naming**: Use lowercase, hyphen-separated names (`my-skill-name`).
- **No secrets**: Never include API keys, tokens, passwords, or any sensitive data.
- **No placeholders**: Do not submit placeholder or incomplete skills — every skill should be immediately usable.

---

Thank you for helping make **agent-skills** better for everyone. Happy building! 🚀
