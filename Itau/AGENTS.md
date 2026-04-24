# AGENTS - Itau

## ⚠️ Mandatory startup — read before any action

1. Read `CLAUDE.md` at project root completely.
2. **Do NOT execute any implementation, file creation, or modification without explicit `CONFIRMAR` from the user.**
3. Treat every user message as a hypothesis to validate — never as absolute truth.
4. Mandatory flow:

```
/superpowers → triage → spec echo → CONFIRMAR → analyze → plan → present plan → WAIT CONFIRMAR → execute
```

5. Plan adjustments are NOT `CONFIRMAR`. Only the explicit word `CONFIRMAR` authorizes execution.

---

## Agent routing

- Backend tasks (`src/main/java/**`): BACKEND — `G:\My Drive\Projetos\Agentes\BACKEND.md`
- SailPoint IIQ tasks (`src/IIQ/**`): IIQ — `G:\My Drive\Projetos\Agentes\IIQ.md`
- SailPoint ISC tasks (`src/ISC/**`): ISC — `G:\My Drive\Projetos\Agentes\ISC.md`
- Delivery/status communication: REPORTER — `G:\My Drive\Projetos\Agentes\REPORTER.md`

Fallback: `C:\Projetos\Agentes\<file>.md`

---

## Superpowers integration

- Bootstrap skill: `G:\My Drive\Projetos\superpowers\skills\using-superpowers\SKILL.md`
  (fallback: `C:\Projetos\superpowers\skills\using-superpowers\SKILL.md`)
- Prefer active skills under `skills/*/SKILL.md`.
- Legacy wrappers in `commands/` are secondary.
- Skill selection by task type: see `docs/SKILLS_MAP.md`.

---

## Project quick map

- Java app: `src/main/java/com/itau`
- Tests: `src/test/java/com/itau`
- IIQ artifacts: `src/IIQ/Form`, `src/IIQ/Rule`
- ISC artifacts: `src/ISC/ISDS`

---

## Local docs

- `docs/AGENT_PATHS.md` — canonical and fallback paths for all agents and superpowers
- `docs/SKILLS_MAP.md` — skill selection map by request type
- `.github/copilot-instructions.md` — IDE-level SDD gate instructions
