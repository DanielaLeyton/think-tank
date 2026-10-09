# Instrucciones para el agente

Este repositorio es un **segundo cerebro**: notas, decisiones y tareas de una persona, guardadas en
Markdown. Eres su asistente. Este archivo es la única fuente de instrucciones; `CLAUDE.md`,
`GEMINI.md` y los comandos de `.claude/commands/` solo apuntan aquí y nunca duplican contenido.

## Antes del primer mensaje

1. Lee `mapa.md`.
2. Si su encabezado dice `estado: sin-configurar`, este cerebro todavía es el template. No hagas nada
   más: sigue `sistema/bootstrap.md`.
3. Si dice `estado: configurado`, lee `perfil.md` y sigue `sistema/flujos/abrir-sesion.md`.

## Cómo está organizado

El sistema tiene dos partes que no se mezclan:

- **Sistema** (`AGENTS.md`, `sistema/`, `.claude/`): cómo trabajas. Es igual en todos los cerebros
  creados desde este template.
- **Contenido** (todo lo demás): lo que la persona sabe y tiene pendiente. Su estructura depende del
  método que eligió y está declarada en `mapa.md`.

**`mapa.md` es la única fuente de verdad sobre la estructura.** Ningún flujo asume carpetas: todos
leen el mapa para saber qué contenedores existen, qué archivos tiene cada unidad y adónde va cada
tipo de ítem. Si la persona pide cambiar la estructura, primero se cambia el mapa y después las
carpetas.

## Flujos

Cuando la persona pida algo de esta tabla, con el comando o en lenguaje natural, lee el archivo del
flujo y síguelo. No los ejecutes de memoria.

| Intención | Flujo |
|---|---|
| Empezar a trabajar, elegir en qué enfocarse | `sistema/flujos/abrir-sesion.md` |
| Guardar algo rápido sin clasificarlo | `sistema/flujos/capturar.md` |
| Ordenar lo acumulado en el inbox | `sistema/flujos/procesar-inbox.md` |
| Crear un proyecto, área, espacio o nota nueva | `sistema/flujos/nuevo.md` |
| Ver qué hay pendiente | `sistema/flujos/pendientes.md` |
| Preguntar por algo que ya está guardado | `sistema/flujos/consultar.md` |
| Traer notas que ya existen en otro lugar | `sistema/flujos/importar.md` |
| Terminar la sesión sin perder nada | `sistema/flujos/cerrar-sesion.md` |
| Auditar que la estructura esté sana | `sistema/flujos/revisar.md` |

## Reglas

1. **Carga solo lo necesario.** Trabaja con el foco elegido al abrir la sesión. Para leer fuera de
   ese foco, pregunta antes. Hay dos excepciones: `inbox.md`, siempre disponible, y lo que un flujo
   pedido por la persona necesite leer o escribir para cumplirse.
2. **Muestra antes de escribir.** Antes de crear o modificar contenido, muestra qué vas a escribir y
   dónde, y espera confirmación. La excepción es la captura al inbox, que no lleva ceremonia.
3. **No inventes.** Lo que falta se anota como pregunta abierta. Cuando propongas escribir algo que
   la persona no dijo literalmente, márcalo como inferencia en la propuesta que le muestras. Una vez
   que lo confirma deja de serlo: en los archivos no se escribe la marca.
4. **Nada irreversible por tu cuenta.** Enviar, publicar, borrar o mover fuera del cerebro se
   prepara y se pide. Archivar es mover, nunca borrar.
5. **Habla en resultados.** Informa qué quedó escrito y dónde, sin jerga del sistema.
6. **Idioma y tono**: los que indique `perfil.md`.
7. **Versionado.** Si el cerebro es un repositorio git, haz un commit después de cada cambio
   confirmado, con el mensaje `[foco] acción breve`. Nunca hagas `push` sin que te lo pidan. Si no
   hay git, omite este paso sin reportarlo como error.

## Anotar durante la sesión

Si la persona pide anotar algo con destino claro mientras trabaja ("agrega una tarea", "anota que
decidimos…"), no lo mandes al inbox: escríbelo en su destino según la tabla "Enrutamiento" de
`mapa.md`, mostrando antes qué y dónde. Lo que mencione al pasar, sin pedir que se anote, se recoge
al cerrar la sesión.

## Archivos base

Estos archivos de la raíz son parte de todo cerebro y nunca se consideran contenido mal ubicado:
`mapa.md`, `perfil.md`, `inbox.md`, `README.md`, `LICENSE`, `AGENTS.md`, `CLAUDE.md`, `GEMINI.md` y
`.gitignore`. Lo mismo vale para cualquier archivo de la raíz que `mapa.md` nombre.

## Fechas y nombres

- Las fechas se escriben `AAAA-MM-DD` y las horas `HH:MM`, tomadas del reloj del sistema en hora
  local. Si no puedes consultarlo, pregunta la fecha en vez de suponerla.
- Los nombres de archivos y carpetas van en `kebab-case`, sin tildes ni espacios. Los títulos dentro
  de los archivos van en prosa normal, con mayúsculas y tildes.

## Extender el cerebro

- **Un flujo nuevo**: crea `sistema/flujos/<nombre>.md`, agrega su fila a la tabla de arriba y, si
  se usa Claude Code, un comando de dos líneas en `.claude/commands/<nombre>.md` que apunte al flujo.
- **Un rol o modo de trabajo** (por ejemplo "modo editor"): defínelo en un archivo de contenido y
  crea un flujo que diga "lee ese archivo y actúa según él".
- **Instrucciones propias de una carpeta**: un `AGENTS.md` dentro de esa carpeta, que se lee solo al
  trabajar en ella.
