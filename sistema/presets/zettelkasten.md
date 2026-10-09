# Preset: Zettelkasten

**Úsalo si** tu objetivo es pensar y escribir: investigación, estudio, una tesis, un libro. Organiza
por ideas enlazadas entre sí, no por tareas.

## Estructura

```
notas/     Notas permanentes: una idea por nota, escrita con tus palabras
fuentes/   Una nota por libro, artículo, charla o video, con lo que sacaste de ahí
indices/   Puntos de entrada a un tema: listas comentadas de enlaces a notas
```

Las notas fugaces viven en `inbox.md`. Las tareas van en un solo `tareas.md` en la raíz.

## Preguntas del bootstrap

- ¿Sobre qué temas vas a escribir? Se crea un índice por cada uno.

Crea además `tareas.md` en la raíz con el título `# Tareas`.

## Mapa

Copia este bloque completo como `mapa.md`.

````markdown
---
estado: configurado
preset: zettelkasten
---

# Mapa

## Contenedores

| Carpeta | Qué guarda | Unidad | Plantilla | foco | archivar |
|---|---|---|---|---|---|
| `indices/` | Puntos de entrada por tema | Archivo | `sistema/plantillas/indice.md` | sí | no |
| `notas/` | Una idea por nota | Archivo | `sistema/plantillas/nota.md` | no | no |
| `fuentes/` | Una nota por fuente consultada | Archivo | `sistema/plantillas/fuente.md` | no | no |

## Al enfocar

El índice elegido. Las notas que enlaza se abren solo cuando la conversación las necesita.

## Enrutamiento

| Tipo | Destino | Formato |
|---|---|---|
| Idea | `notas/<titulo-como-afirmacion>.md` | Nota nueva, una sola idea, con al menos un enlace |
| Cita o resumen de una fuente | `fuentes/<autor-titulo>.md` | Se agrega a la nota de esa fuente |
| Tarea | `tareas.md` en la raíz | `- [ ] Descripción (vence: AAAA-MM-DD)` |
| Tema nuevo | `indices/<tema>.md` | Índice nuevo |

Reglas de las notas:

- El título es una afirmación, no un tema: "La repetición espaciada vence al repaso masivo".
- Los enlaces usan `[[nombre-del-archivo]]` y cada uno lleva una frase que explica la relación.
- Antes de crear una nota, busca si ya existe una sobre la misma idea y propón ampliarla.
- Toda nota nueva se agrega al menos a un índice.

## Al cerrar

Las ideas se proponen como notas nuevas o ampliaciones de notas existentes. Las tareas van a
`tareas.md`. Las preguntas abiertas van al índice en foco, sección "Preguntas abiertas". No hay
bitácora.

## Archivado

No se archiva. Una nota superada se enlaza a la que la reemplaza con una línea
`Reemplazada por [[otra-nota]]` al inicio.

## Revisión

- Notas huérfanas: ninguna otra nota ni índice las enlaza.
- Notas con más de una idea, candidatas a dividirse.
- Enlaces `[[…]]` que apuntan a archivos que no existen.
````
