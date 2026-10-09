# Preset: Espacios

**Úsalo si** trabajas en varios contextos que no deben mezclarse: clientes, empresas, productos o
roles distintos. Cada espacio está aislado y tiene sus propias iniciativas.

## Estructura

```
espacios/
  <espacio>/
    contexto.md      Qué es, quiénes participan, decisiones
    tareas.md
    bitacora.md
    iniciativas/     Trabajo con resultado concreto dentro del espacio
    notas/           Referencia propia del espacio
archivo/             Espacios e iniciativas terminados
```

## Preguntas del bootstrap

- ¿En qué espacios trabajas? Nombres separados por comas.

Por cada espacio, crea además sus carpetas `iniciativas/` y `notas/`.

## Mapa

Copia este bloque completo como `mapa.md`.

````markdown
---
estado: configurado
preset: espacios
---

# Mapa

## Contenedores

| Carpeta | Qué guarda | Unidad | Plantilla | foco | archivar |
|---|---|---|---|---|---|
| `espacios/` | Contextos aislados entre sí | Carpeta | `sistema/plantillas/unidad/` | sí | sí |
| `espacios/*/iniciativas/` | Trabajo con resultado y final | Carpeta | `sistema/plantillas/unidad/` | sí | sí |
| `espacios/*/notas/` | Referencia del espacio | Archivo | `sistema/plantillas/nota.md` | no | no |
| `archivo/` | Lo terminado | — | — | no | — |

Al crear un espacio, crea también sus carpetas `iniciativas/` y `notas/`.

## Al enfocar

Un espacio: su `tareas.md`, la última entrada de `bitacora.md` y la lista de nombres de sus
iniciativas. Una iniciativa: lo mismo de la iniciativa, más el `contexto.md` de su espacio.

**Aislamiento**: con un espacio en foco, no leas ni escribas en otro espacio. Si la persona menciona
algo de otro espacio, captúralo al inbox.

## Enrutamiento

| Tipo | Destino | Formato |
|---|---|---|
| Tarea | `tareas.md` de la iniciativa, o del espacio si no pertenece a ninguna | `- [ ] Descripción (vence: AAAA-MM-DD)` |
| Decisión | `contexto.md`, sección "Decisiones" | `- **AAAA-MM-DD**: decisión y razón` |
| Aprendizaje | `contexto.md`, sección "Aprendizajes" | Una línea |
| Referencia | `notas/<tema>.md` del espacio | Nota con su fuente |
| Persona | `contexto.md` del espacio, sección "Personas" | `- **Nombre**: rol y qué le importa` |

## Al cerrar

Todo se escribe en la unidad en foco: decisiones y aprendizajes a `contexto.md`, tareas a
`tareas.md`, preguntas abiertas a "Preguntas abiertas" de `contexto.md`, y la entrada de sesión a
`bitacora.md`.

## Archivado

Una iniciativa terminada se mueve a `archivo/<espacio>/<iniciativa>/`. Un espacio cerrado se mueve
completo a `archivo/<espacio>/`.

## Revisión

- Tareas en el `tareas.md` de un espacio que pertenecen a una de sus iniciativas.
- Menciones al nombre de un espacio dentro de otro, como señal de contexto filtrado.
````
