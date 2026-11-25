# Verification Engineering — Agent Skill

> *"Prompt engineering is dead. Welcome to Verification Engineering."*

Uma skill autônoma de agente em malha fechada para **Google Antigravity** (compatível com Claude Code, Cursor e OpenCode) que aplica um fluxo de **Curadoria de Contexto -> Plano Somente Leitura -> Loop Oráculo Determinístico -> Auditoria de Invariantes** em bases de código novas ou legadas.

## Por que Verification Engineering?

O fluxo foca em mudar o papel humano de codificação para auditoria arquitetural em quatro etapas:
1. **Curadoria de Contexto:** Inspeciona apenas arquivos-alvo para evitar excesso de ruído.
2. **Planejamento Somente Leitura:** Exige um planejamento sem edições prévias no estado.
3. **Loop Oráculo Determinístico:** Define critérios objetivos de saída (testes unitários, linter) com limite de 4 tentativas.
4. **Auditoria de Invariantes:** Revisa o `git diff` para integridade e segurança.

## Instalação rápida

* **Global (macOS/Linux):**
  `mkdir -p ~/.gemini/config/skills/verification-engineering && curl -o ~/.gemini/config/skills/verification-engineering/SKILL.md https://githubusercontent.com`
* **Global (Windows PowerShell):**
  `New-Item -ItemType Directory -Force -Path "$env:USERPROFILE\.gemini\config\skills\verification-engineering" ; Invoke-WebRequest -Uri "https://githubusercontent.com" -OutFile "$env:USERPROFILE\.gemini\config\skills\verification-engineering\SKILL.md"`
* **Por projeto:** Copie o arquivo `SKILL.md` para `.gemini/skills/verification-engineering/SKILL.md` no seu repositório.

## Uso

O agente aciona o protocolo automaticamente ou via comando explícito:
`/verification-engineering [tarefa]`

## Licença
MIT
