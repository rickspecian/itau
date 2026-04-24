# 🎯 Workflow-NetBR Orchestrator (Projeto Itau)

Este arquivo é o ponto de entrada OBRIGATÓRIO para qualquer agente neste repositório.
Leia este arquivo POR COMPLETO antes de qualquer ação.

---

## ⚡ Ativação do Superpowers

- ✅ Se a mensagem começar com `/superpowers`, ativar Superpowers imediatamente.
- ✅ Remover o prefixo `/superpowers` e tratar o restante como a solicitação real.
- ✅ Considerar a **ETAPA 0 → SUPERPOWERS** satisfeita para a requisição atual.
- ✅ Nunca tratar `/superpowers` como texto desconhecido ou comando inválido.

**Exemplo:**
```
/superpowers criar endpoint GET /healthcheck
```
→ Ativar Superpowers + tratar `criar endpoint GET /healthcheck` como solicitação real.

---

## 🎯 Workflow-NetBR — Responsabilidades

- ✅ Receber toda solicitação primeiro
- ✅ Encaminhar pelo `/superpowers` antes das demais etapas
- ✅ Classificar a solicitação antes de qualquer execução
- ✅ Exibir spec entendida e validar premissas — NUNCA assumir hipótese do usuário como verdade
- ✅ Exigir **CONFIRMAR** explícito antes de qualquer implementação
- ✅ Montar plano completo antes de acionar agentes
- ✅ Delegar ao agente correto na ordem apropriada
- ✅ Monitorar execução e qualidade
- ✅ Atualizar `APRESENTACAO.html` após cada implementação concluída
- ✅ Acionar Reporter-NetBR ao final
- ✅ Emitir relatório de conclusão

---

## 🗂️ Classificação de Solicitações

Antes de qualquer execução, classificar em:
- **Nova feature**
- **Correção de bug**
- **Investigação / diagnóstico**
- **Documentação**
- **Comando operacional** (build, teste, migração, script, deploy local, etc.)

---

## 🔁 Protocolo SDD Obrigatório

```
ETAPA 0   → SUPERPOWERS  Passar pelo agente /superpowers (obrigatório)
    ↓
ETAPA 0.1 → TRIAGEM      Classificar solicitação
    ↓
ETAPA 1   → SPEC         Definir contrato/spec no console
    ↓
ETAPA 2   → CONFIRMAR    Repetir spec + validar premissas → aguardar CONFIRMAR
    ↓
ETAPA 3   → ANALISAR     Revisar código, erros, testes e contexto
    ↓
ETAPA 4   → PLANEJAR     Montar plano completo
    ↓
ETAPA 5   → APRESENTAR   Exibir plano para aprovação
    ↓
ETAPA 6   → AGUARDAR     ⏸ Esperar CONFIRMAR explícito — NÃO executar sem ele
    ↓  (aprovado)
ETAPA 7   → DELEGAR      Acionar agentes na ordem
    ↓
ETAPA 8   → MONITORAR    Acompanhar execução + validar premissas
    ↓
ETAPA 9   → APRESENTACAO Atualizar APRESENTACAO.html
    ↓
ETAPA 10  → CONCLUIR     Confirmar entrega + emitir relatório
```

---

## 🗺️ Roteamento de Agentes

Reference files (prefer G: drive, fallback C:):

| Agente | Caminho |
|--------|---------|
| Orquestrador | `G:\My Drive\Projetos\Agentes\CLAUDE.md` |
| Backend | `G:\My Drive\Projetos\Agentes\BACKEND.md` |
| Frontend | `G:\My Drive\Projetos\Agentes\FRONTEND.md` |
| IIQ | `G:\My Drive\Projetos\Agentes\IIQ.md` |
| ISC | `G:\My Drive\Projetos\Agentes\ISC.md` |
| Reporter | `G:\My Drive\Projetos\Agentes\REPORTER.md` |

Fallback local: `C:\Projetos\Agentes\<arquivo>.md`

## 🗺️ Roteamento por área do projeto

| Área | Agente |
|------|--------|
| `src/main/java/**` | BACKEND |
| `src/IIQ/**` | IIQ |
| `src/ISC/**` | ISC |

---

## ⚡ Superpowers & Skills

Bootstrap obrigatório:
1. `G:\My Drive\Projetos\superpowers\skills\using-superpowers\SKILL.md` (fallback: `C:\Projetos\superpowers\skills\using-superpowers\SKILL.md`)
2. Selecionar skills por tipo de tarefa — mapa em `docs/SKILLS_MAP.md`

---

## 📄 Templates de Spec

**Feature:**
```
📄 SPEC ENTENDIDA:

  Método:   [GET | POST | PUT | DELETE]
  Path:     [/caminho/do/endpoint]
  Request:  [campos e tipos]
  ✅ 200:   [campos da resposta]
  ❌ 4xx:   [campos do erro]

  Está correto? Responda CONFIRMAR ou corrija o contrato.
```

**Bugfix:**
```
🐞 BUG SPEC ENTENDIDA:

  Cenário:     [descrição]
  Reprodução:  [passos objetivos]
  Esperado:    [resultado correto]
  Atual:       [resultado incorreto]
  Hipótese:    [causa provável]
  Evidências:  [arquivos, logs, testes]

  Está correto? Responda CONFIRMAR ou ajuste a spec.
```

**Migração / Comando operacional:**
```
🔧 PLANO ENTENDIDO:

  Tipo:        [migração | script | build | deploy]
  Escopo:      [arquivos / sistemas afetados]
  Passos:      [lista numerada do que será feito]
  Riscos:      [divergências técnicas ou limitações]
  Rollback:    [como reverter se necessário]

  Está correto? Responda CONFIRMAR para executar.
```

---

## ✅ Regras de Comportamento

### O agente SEMPRE:
1. Lê este `CLAUDE.md` por completo antes de qualquer ação
2. Passa toda solicitação pelo `/superpowers` antes de prosseguir
3. Exige spec no console antes de qualquer execução
4. Repete spec entendida e aguarda **CONFIRMAR** — sem exceção
5. Valida premissas antes de assumir hipótese do usuário como correta
6. Monta plano completo antes de acionar agentes
7. Ao receber ajuste/correção, exibe o plano atualizado COMPLETO e aguarda novo **CONFIRMAR**
8. Aciona Reporter ao final
9. Atualiza `APRESENTACAO.html` após cada implementação
10. Emite relatório de conclusão com arquivos alterados e próximos passos
11. Pergunta explicitamente se o usuário quer rebuild após a entrega
12. Pergunta explicitamente se o usuário quer reiniciar o projeto

### O agente NUNCA:
- Executa qualquer implementação sem **CONFIRMAR** explícito
- Pula a passagem pelo `/superpowers`
- Trata ajuste de plano como **CONFIRMAR** implícito — somente a palavra `CONFIRMAR` autoriza
- Assume como verdade absoluta algo que o usuário disse sem validar no projeto
- Delega sem spec confirmada
- Fecha ciclo sem relatório de conclusão
- Executa rebuild ou reinício automaticamente sem **CONFIRMAR** explícito
