# Preset: PARA

**Úsalo si** quieres organizar tu trabajo y tu vida por lo que tienes que hacer: proyectos con fecha
de término y responsabilidades permanentes. Es el método de Tiago Forte y el más fácil para empezar.

## Estructura

```
proyectos/   Trabajo activo con un resultado concreto y un final
areas/       Responsabilidades permanentes, sin final (salud, finanzas, equipo)
recursos/    Material de referencia sobre temas de interés
archivo/     Lo terminado o pausado
```

## Preguntas del bootstrap

- ¿Qué áreas quieres crear ahora? Nombres separados por comas.
- ¿Qué proyectos tienes activos hoy? Para cada uno, qué resultado busca y para cuándo. Si no lo
  sabe todavía, queda vacío.

## Mapa

Copia este bloque completo como `mapa.md`.

````markdown
---
estado: configurado
preset: para
---

# Mapa

## Contenedores

| Carpeta | Qué guarda | Unidad | Plantilla | foco | archivar |
|---|---|---|---|---|---|
| `proyectos/` | Trabajo activo con resultado y final | Carpeta | `sistema/plantillas/unidad/` | sí | sí |
| `areas/` | Responsabilidades permanentes | Carpeta | `sistema/plantillas/unidad/` | sí | no |
| `recursos/` | Material de referencia | Archivo | `sistema/plantillas/nota.md` | no | no |
| `archivo/` | Lo terminado o pausado | — | — | no | — |

## Al enfocar

Proyectos y áreas: `tareas.md`, luego la última entrada de `bitacora.md`. `contexto.md` solo si la
tarea lo necesita.

## Enrutamiento

| Tipo | Destino | Formato |
|---|---|---|
| Tarea | `tareas.md` de la unidad | `- [ ] Descripción (vence: AAAA-MM-DD)` |
| Decisión | `contexto.md` de la unidad, sección "Decisiones" | `- **AAAA-MM-DD**: decisión y razón` |
| Aprendizaje | `contexto.md` de la unidad, sección "Aprendizajes" | Una línea |
| Referencia | `recursos/<tema>.md` | Nota con su fuente |
| Idea | `recursos/ideas.md` | `- **AAAA-MM-DD**: la idea en una línea` |

## Al cerrar

Decisiones y aprendizajes a `contexto.md`, tareas a `tareas.md`, preguntas abiertas a la sección
"Preguntas abiertas" de `contexto.md`, y la entrada de sesión a `bitacora.md`.

## Archivado

Un proyecto terminado o pausado se mueve completo a `archivo/<nombre>/`. Las áreas no se archivan.

## Revisión

- Proyectos sin fecha de término ni resultado definido en `contexto.md`: ¿son en realidad áreas?
- Áreas sin ninguna tarea ni entrada de bitácora en 90 días.
````
