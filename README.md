# Verification Engineering — Agent Skill

> *"Prompt engineering is dead. Welcome to Verification Engineering."*

An autonomous, closed-loop agent skill designed for **Google Antigravity** (and compatible with Claude Code, Cursor, and OpenCode). It enforces a strict **Curate Context → Read-Only Plan → Deterministic Oracle Loop → Invariant Audit** workflow across both greenfield and legacy codebases.

## Why Verification Engineering?

Most AI coding workflows fail because the model rushes into writing code without context or a way to verify its own output—leaving the human developer to copy-paste terminal errors back into the chat.

This skill shifts the human role from **writing syntax** to **auditing architecture and invariants**:

1. **Context Curation (High Signal > Noise):** Inspects manifests and target files only—no context bloat.
2. **Read-Only Discovery & Planning:** Forces a strict zero-edit planning phase before touching state.
3. **Deterministic Oracle Loop:** Requires defining an objective exit criterion (unit tests, compiler, or linter) and autonomously iterates until all checks pass (with a 4-retry circuit breaker).
4. **Invariant Audit:** Reviews `git diff` for business logic integrity, security boundaries, and clean resource disposal.

## Installation (Google Antigravity)

### Global Install (Recommended — applies to all current and future projects)

**macOS / Linux:**
```bash
mkdir -p ~/.gemini/config/skills/verification-engineering
curl -o ~/.gemini/config/skills/verification-engineering/SKILL.md https://githubusercontent.com
```

**Windows (PowerShell):**
```powershell
New-Item -ItemType Directory -Force -Path "$env:USERPROFILE\.gemini\config\skills\verification-engineering"
Invoke-WebRequest -Uri "https://githubusercontent.com" -OutFile "$env:USERPROFILE\.gemini\config\skills\verification-engineering\SKILL.md"
```

### Project-Specific Install
Copy `SKILL.md` into your repository's `.gemini/skills/verification-engineering/SKILL.md` folder.

## Usage

Once installed, the agent automatically triggers the protocol on feature builds, bug fixes, and refactors. You can also invoke it explicitly:

```text
/verification-engineering Build a REST API endpoint with integration tests
```

## License

MIT
# verification-engineering-skill
