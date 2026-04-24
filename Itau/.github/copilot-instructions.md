# Copilot Instructions - Itau

## ⚠️ REGRA ABSOLUTA — Leia antes de qualquer ação

1. **Ler `CLAUDE.md`** na raiz do projeto SEMPRE antes de qualquer ação.
2. **NUNCA executar código, criar arquivos ou modificar artefatos sem `CONFIRMAR` explícito do usuário.**
3. O fluxo obrigatório é:

```
/superpowers → triagem → spec → CONFIRMAR → analisar → planejar → apresentar → AGUARDAR CONFIRMAR → executar
```

4. Ajuste ou correção de plano NÃO é `CONFIRMAR`. Somente a palavra `CONFIRMAR` autoriza execução.

---

## Roteamento por área

- `src/main/java/**` → BACKEND (`G:\My Drive\Projetos\Agentes\BACKEND.md`)
- `src/IIQ/**` → IIQ (`G:\My Drive\Projetos\Agentes\IIQ.md`)
- `src/ISC/**` → ISC (`G:\My Drive\Projetos\Agentes\ISC.md`)
- Comunicação de entrega → REPORTER (`G:\My Drive\Projetos\Agentes\REPORTER.md`)

Fallback: `C:\Projetos\Agentes\<arquivo>.md`

---

## Superpowers

- Bootstrap: `G:\My Drive\Projetos\superpowers\skills\using-superpowers\SKILL.md`
  (fallback: `C:\Projetos\superpowers\skills\using-superpowers\SKILL.md`)
- Seleção de skill por tipo: ver `docs/SKILLS_MAP.md`
- Prompt com prefixo `/superpowers` ativa o modo Superpowers imediatamente.

---

## Paths de referência

- Agentes e caminhos canônicos: `docs/AGENT_PATHS.md`
- Mapa de skills: `docs/SKILLS_MAP.md`
