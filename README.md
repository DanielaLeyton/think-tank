# think-tank

Una base para crear tu segundo cerebro: una carpeta de archivos Markdown que un agente de IA
mantiene contigo. Capturas lo que se te ocurre, el agente lo ordena, y cada sesión parte donde
terminó la anterior.

No impone un método. Al configurarlo eliges cómo organizarte, y puedes crear tantos cerebros como
necesites, cada uno con el suyo.

## Qué trae

- **Un núcleo de nueve flujos** que funcionan igual con cualquier método: abrir sesión, capturar,
  procesar el inbox, crear, ver pendientes, consultar, importar, cerrar sesión y revisar.
- **Parte con lo que ya tienes**: importa tus notas de Notion, Obsidian, Apple Notes o una carpeta
  cualquiera, y el agente propone dónde va cada cosa.
- **Pregúntale a tu cerebro**: "¿qué decidimos sobre precios?" se responde con lo que guardaste,
  citando el archivo de donde sale cada dato.
- **Cuatro métodos listos**: PARA, Zettelkasten, Espacios y Libre.
- **Instrucciones para varios agentes**: Claude Code, Codex, Cursor, Gemini CLI y cualquiera que lea
  `AGENTS.md`.
- **Solo Markdown**: sin instalador, sin scripts y sin dependencias. Git es opcional.

## Empezar

1. Crea tu copia con **Use this template** en GitHub, o clona y renombra:

   ```bash
   git clone https://github.com/DanielaLeyton/think-tank.git mi-cerebro
   ```

   Sin git, descarga el ZIP y descomprímelo.

2. Abre tu agente en esa carpeta y escribe:

   > Configura mi cerebro.

   En Claude Code también funciona `/configurar`.

3. Responde la entrevista: quién eres, para qué es este cerebro y qué método quieres. El agente crea
   las carpetas y deja todo listo.

4. Si ya tienes notas en otro lugar, tráelas:

   > Importa mis notas de ~/Documentos/mi-exportacion

   El agente hace un inventario, propone un plan y espera tu aprobación. Tus archivos originales no
   se modifican.

## Métodos

| Método | Úsalo si | Organiza por |
|---|---|---|
| **PARA** | Quieres ordenar trabajo y vida por lo que tienes que hacer | Proyectos, áreas, recursos y archivo |
| **Zettelkasten** | Tu objetivo es pensar y escribir: investigación, tesis, un libro | Notas de una idea enlazadas entre sí |
| **Espacios** | Trabajas en contextos que no deben mezclarse: clientes, empresas, roles | Espacios aislados con sus iniciativas |
| **Libre** | Ya tienes tu sistema o quieres que aparezca con el uso | Lo que tú declares |

## Uso diario

Puedes pedirlo en lenguaje natural o, en Claude Code, con el comando.

| Qué quieres | Dilo así | Comando |
|---|---|---|
| Elegir en qué trabajar | "Trabajemos en …" | `/abrir-sesion` |
| Guardar algo rápido | "Captura: …" | `/capturar` |
| Ordenar lo capturado | "Procesa el inbox" | `/procesar-inbox` |
| Crear un proyecto, espacio o nota | "Crea un proyecto …" | `/nuevo` |
| Ver tareas abiertas | "¿Qué tengo pendiente?" | `/pendientes` |
| Preguntar por algo guardado | "¿Qué decidimos sobre …?" | `/consultar` |
| Traer notas de otro lugar | "Importa mis notas de …" | `/importar` |
| Terminar sin perder nada | "Cierra la sesión" | `/cerrar-sesion` |
| Detectar desorden | "Revisa el cerebro" | `/revisar` |

## Cómo funciona

```
mi-cerebro/
├── AGENTS.md          Instrucciones del agente (única fuente)
├── CLAUDE.md          Apunta a AGENTS.md
├── GEMINI.md          Apunta a AGENTS.md
├── mapa.md            La estructura de este cerebro
├── perfil.md          Quién eres y cómo quieres que te respondan
├── inbox.md           Captura sin clasificar
├── sistema/
│   ├── bootstrap.md   La entrevista de configuración
│   ├── flujos/        Los nueve flujos del núcleo
│   ├── presets/       Un archivo por método
│   └── plantillas/    Archivos base de cada unidad
├── .claude/commands/  Comandos de Claude Code, de dos líneas cada uno
└── …                  Tus carpetas, según el método elegido
```

La pieza central es `mapa.md`. Declara qué carpetas existen, qué archivos tiene cada unidad y adónde
va cada tipo de ítem. Los flujos no conocen ningún método: leen el mapa. Por eso el mismo núcleo
sirve para PARA y para Zettelkasten, y por eso cambiar la estructura es editar un archivo.

Todo lo que no está en `sistema/`, `.claude/` ni en los archivos de instrucciones es contenido tuyo.

## Adaptarlo

- **Cambiar la estructura**: edita `mapa.md` o pídeselo al agente. Agregar una carpeta es agregar una
  fila a la tabla "Contenedores".
- **Agregar un método**: copia un archivo de `sistema/presets/`, ajusta sus secciones y agrégalo a la
  tabla de `sistema/bootstrap.md`.
- **Agregar un flujo**: crea `sistema/flujos/<nombre>.md` y súmalo a la tabla de `AGENTS.md`.
- **Varios cerebros**: crea una copia del template por cada propósito. Son independientes entre sí.

## Agentes compatibles

| Agente | Qué lee |
|---|---|
| Claude Code | `CLAUDE.md`, que importa `AGENTS.md`, y los comandos de `.claude/commands/` |
| Codex, Cursor, Copilot y otros | `AGENTS.md` directamente |
| Gemini CLI | `GEMINI.md`, que remite a `AGENTS.md` |

Los comandos con `/` solo existen en Claude Code. En los demás agentes, los mismos flujos se piden en
lenguaje natural.

## Visualización opcional

La carpeta se puede abrir como bóveda de [Obsidian](https://obsidian.md/). Las tareas usan casillas
`- [ ]` y los enlaces del método Zettelkasten usan `[[nota]]`, ambos formatos nativos de Obsidian.

## Licencia

MIT. Ver [LICENSE](LICENSE).
