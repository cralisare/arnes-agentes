# Plantillas para agentes IA

Kit mínimo de plantillas para configurar agentes de IA (Claude Code, Gemini, Codex, Cursor) de forma coherente en todos tus proyectos.

Tres archivos. Uno por capa.

## Qué contiene

| Archivo | Para qué sirve | Dónde vive |
|---|---|---|
| [`CLAUDE.md`](CLAUDE.md) | **Contexto global del usuario.** Quién eres, cómo trabajas, principios de código, reglas de secretos. Una sola vez por máquina. | `~/.claude/CLAUDE.md` |
| [`AGENTS.md`](AGENTS.md) | **Contexto por proyecto.** Stack, comandos, mapa del repo, convenciones, reglas duras. Una copia en cada proyecto. | Raíz del proyecto |
| [`MEMORY.md`](MEMORY.md) | **Índice de memoria persistente.** Apunta a archivos `feedback_*` / `project_*` / `reference_*` con cosas aprendidas durante el trabajo. Opcional por proyecto. | Raíz del proyecto |

## Filosofía

- **Mapa, no biblia.** Las plantillas son índices navegables, no manuales para leer de cabo a rabo.
- **Multi-agente por defecto.** Convención `AGENTS.md` para que cualquier agente lea las mismas reglas. Symlinks `CLAUDE.md` y `GEMINI.md` apuntan al canónico.
- **Sin scaffolding obligatorio.** Sin scripts, sin JSONs, sin estructura de carpetas forzada. Pegar y rellenar.
- **No duplicar el global.** Cada plantilla asume lo que ya saben los agentes desde el global y solo añade lo específico de su capa.
- **Cuándo este archivo miente.** Las plantillas envejecen. Cada una incluye una pauta para que el agente verifique contra el código y avise si hay discrepancias.

## Cómo usar

### 1. Contexto global (una sola vez)

```bash
mkdir -p ~/.claude
cp CLAUDE.md ~/.claude/CLAUDE.md
