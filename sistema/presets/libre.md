# Preset: Libre

**Úsalo si** ya tienes tu propia forma de organizarte o quieres que la estructura aparezca con el
uso. Parte con lo mínimo y el mapa crece cuando lo pidas.

## Estructura

```
notas/   Todo lo que no es tarea
```

Las tareas van en un solo `tareas.md` en la raíz.

## Preguntas del bootstrap

- ¿Ya tienes carpetas o categorías en mente? Si las nombra, agrega una fila por cada una a la tabla
  "Contenedores" del mapa, preguntando si cada unidad es una carpeta con seguimiento (contexto,
  tareas y bitácora) o un archivo suelto.

Crea además `tareas.md` en la raíz con el título `# Tareas`.

## Mapa

Copia este bloque completo como `mapa.md`.

````markdown
---
estado: configurado
preset: libre
---

# Mapa

## Contenedores

| Carpeta | Qué guarda | Unidad | Plantilla | foco | archivar |
|---|---|---|---|---|---|
| `notas/` | Todo lo que no es tarea | Archivo | `sistema/plantillas/nota.md` | no | no |

Para agregar un contenedor, suma una fila. Una unidad de tipo Carpeta usa
`sistema/plantillas/unidad/`; una de tipo Archivo usa `sistema/plantillas/nota.md`.

## Al enfocar

Sin contenedores con foco, la sesión parte sin foco: `tareas.md` y la lista de nombres de `notas/`.

## Enrutamiento

| Tipo | Destino | Formato |
|---|---|---|
| Tarea | `tareas.md` en la raíz | `- [ ] Descripción (vence: AAAA-MM-DD)` |
| Cualquier otra cosa | `notas/<tema>.md` | Se agrega a la nota del tema o se crea una |

## Al cerrar

Las tareas van a `tareas.md`. Lo demás se propone como nota nueva o como agregado a una existente.

## Archivado

No hay contenedor de archivo. Si hace falta, agrega la fila `archivo/` a "Contenedores".

## Revisión

- Si hay más de 30 notas en `notas/`, propón agruparlas en contenedores nuevos según sus temas.
````
