# Agent Paths - Itau

## Canonical external paths

Use Google Drive path as primary source when available:

- `G:\My Drive\Projetos\Agentes\CLAUDE.md`
- `G:\My Drive\Projetos\Agentes\BACKEND.md`
- `G:\My Drive\Projetos\Agentes\FRONTEND.md`
- `G:\My Drive\Projetos\Agentes\IIQ.md`
- `G:\My Drive\Projetos\Agentes\ISC.md`
- `G:\My Drive\Projetos\Agentes\REPORTER.md`

Superpowers primary path:

- `G:\My Drive\Projetos\superpowers`

## Local fallback paths (workspace clone)

Use these when G: is not mounted:

- `C:\Projetos\Agentes\CLAUDE.md`
- `C:\Projetos\Agentes\BACKEND.md`
- `C:\Projetos\Agentes\FRONTEND.md`
- `C:\Projetos\Agentes\IIQ.md`
- `C:\Projetos\Agentes\ISC.md`
- `C:\Projetos\Agentes\REPORTER.md`
- `C:\Projetos\superpowers`

## Notes

- In this repository, `CLAUDE.md` at project root is the local orchestrator entrypoint.
- Always resolve path availability first (G: then fallback C:).

