# Verification Engineering — Agent Skill

> *"Prompt engineering is dead. Welcome to Verification Engineering."*

An autonomous, closed-loop agent skill for **Google Antigravity** (compatible with Claude Code, Cursor, and OpenCode) that enforces a strict **Curate Context → Read-Only Plan → Deterministic Oracle Loop → Invariant Audit** workflow across both greenfield and legacy codebases.

## Why Verification Engineering?

This workflow shifts the human role from typing syntax to **architectural auditing** in four phases:

1. **Context Curation (`High Signal > Noise`):** Inspects dependency manifests and target files only—no context bloat.
2. **Read-Only Planning & Oracle Definition:** Forces a zero-edit planning phase (with a Fast-Track for trivial 1-file non-logic edits) and requires a **Fail-First** deterministic oracle.
3. **Closed-Loop Execution:** Iterates against a fast targeted test/module during the 4-retry loop, then runs the full suite/build once before handoff (with strict scope/dependency guardrails).
4. **Invariant Audit:** Reviews `git diff` (or created files directly if no Git repo) for business logic integrity, security boundaries, and clean resource disposal.

## Quick Install

* **Global (macOS / Linux):**
  ```bash
  mkdir -p ~/.gemini/config/skills/verification-engineering && curl -o ~/.gemini/config/skills/verification-engineering/SKILL.md https://raw.githubusercontent.com/bivardourado/verification-engineering-skill/main/SKILL.md
  ```
* **Global (Windows PowerShell):**
  ```powershell
  New-Item -ItemType Directory -Force -Path "$env:USERPROFILE\.gemini\config\skills\verification-engineering" ; Invoke-WebRequest -Uri "https://raw.githubusercontent.com/bivardourado/verification-engineering-skill/main/SKILL.md" -OutFile "$env:USERPROFILE\.gemini\config\skills\verification-engineering\SKILL.md"
  ```
* **Per-Project:** Copy `SKILL.md` into `.gemini/skills/verification-engineering/SKILL.md` in your repository.

## Usage

The agent triggers the protocol automatically on coding tasks, or you can invoke it explicitly:
`/verification-engineering [task]`

## License
MIT
