# AGENTS.md — [ADAPTAR: nombre del proyecto]

> [ADAPTAR: una línea — qué es este proyecto y para quién].
>
> Este archivo es un **mapa**, no una biblia. Lee solo las secciones que necesites para la tarea concreta. Si una sección está vacía o no aplica, bórrala.

> **Para Claude Code**: este archivo se llama `AGENTS.md` por convención multi-agente. Para que se auto-cargue, crea el symlink: `ln -s AGENTS.md CLAUDE.md`.

---

## Antes de empezar

1. Lee este archivo entero — son ~5 minutos.
2. Si hay sección de memoria persistente más abajo, mírala antes de actuar (puede haber decisiones tomadas que no están en el código).
3. Verifica que el proyecto arranca local (ver "Stack y comandos"). Si no arranca, para y dilo — no empieces a tocar sin entorno verde.

---

## Stack y comandos

[ADAPTAR: stack en una línea por capa]

- **Lenguaje / runtime**: [ej. Node 20, Python 3.12, Deno]
- **Frontend**: [ej. vanilla JS + D3, Next.js 15, ninguno]
- **Backend / infra**: [ej. Supabase edge functions, Cloudflare Workers, ninguno]
- **Despliegue**: [ej. Vercel, GitHub Pages, ninguno]

### Comandos esenciales

```bash
# [ADAPTAR: arrancar local]
[ej. python3 -m http.server 8081]

# [ADAPTAR: tests]
[ej. npm test]

# [ADAPTAR: desplegar / publicar]
[ej. git push origin main → Vercel auto-deploy]
```

---

## Mapa del repositorio

| Ruta | Qué contiene | Cuándo leerlo |
|------|--------------|---------------|
| [ADAPTAR: `src/`] | [Código principal] | Casi siempre |
| [ADAPTAR: `data/` o `*.json`] | [Datos persistentes] | Si tocas estructura de datos |
| [ADAPTAR: `docs/`] | [Documentación técnica] | Antes de implementar features nuevas |
| [ADAPTAR: `MEMORY.md` o `.claude/memory/`] | [Memoria persistente del agente] | Al empezar, si existe |

> Borra filas que no apliquen. Añade las que falten. **El criterio no es completitud — es "qué necesita saber un agente nuevo que llega frío"**.

---

## Convenciones de código

- **Idiomas**: [ADAPTAR: ej. variables y funciones en inglés; strings de usuario en español]
- **Naming**: [ADAPTAR: ej. camelCase JS, snake_case Python]
- **Comentarios**: solo donde aportan. No comentar el "qué" si los nombres ya lo dicen.
- **Estilo**: [ADAPTAR: ej. seguir el código existente; no introducir abstracciones especulativas]

---

## Reglas duras

- **Ir al grano**. No repetir lo que ya he dicho.
- **Cambios quirúrgicos**: tocar solo lo necesario para la tarea. No "mejorar" código adyacente.
- **Simplicidad primero**: el mínimo código que resuelve el problema. Sin flexibilidad no solicitada.
- **Si una decisión tiene trade-offs**, dame el criterio — no me des dos opciones para que elija yo.
- **Secretos**: nunca mostrar valores de API keys, tokens, contraseñas, ni anon keys, en el chat. Antes de leer `.env` / `.envrc` / `credentials.*`, avisar.
- **Si te bloqueas o algo no cuadra**, para y dilo antes de seguir.
- [ADAPTAR: añadir reglas específicas del proyecto si las hay]

---

## Memoria persistente *(opcional — borrar si no aplica)*

[ADAPTAR: si el proyecto tiene memoria persistente, describirla aquí.]

Ejemplo:
- `MEMORY.md` — índice de archivos de memoria.
- `feedback_*.md` — lecciones aprendidas, qué funciona y qué no.
- `project_*.md` — estado, deadlines, decisiones.
- `reference_*.md` — URLs, infra, recursos externos.

Mantén estos archivos al día mientras trabajas, no al final.

---

## Cierre de sesión *(opcional — borrar si no aplica)*

Cuando termines un bloque de trabajo:
1. [ADAPTAR: ej. tests verdes / build pasa].
2. Si has aprendido algo no obvio sobre el proyecto, anótalo en la memoria persistente.
3. Si has dejado algo a medias, déjalo claro: archivo + estado + siguiente paso.

---

## Cuándo este archivo miente

Las plantillas envejecen. Si lo que ves en el código contradice lo que dice este archivo:

1. **Confía en el código actual**, no en este archivo.
2. **Avisa** al usuario de la discrepancia antes de actuar.
3. Si la discrepancia es load-bearing, actualiza la sección correspondiente de este archivo en el mismo commit que el cambio.
