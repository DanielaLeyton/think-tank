# Bootstrap

Convierte el template en el cerebro de una persona. Se ejecuta una vez, con una entrevista corta.

Si `mapa.md` ya dice `estado: configurado`, detente y avisa: volver a ejecutarlo reemplaza el mapa.
Continúa solo si la persona lo confirma.

## Entrevista

Pregunta de a un tema por vez. No escribas nada hasta el paso "Confirmar".

1. **Quién es**: nombre y cómo quiere que le hables (idioma, trato, nivel de detalle).
2. **Para qué es este cerebro**: una frase. Por ejemplo "mi trabajo como consultora", "mi tesis",
   "todo lo personal". Una persona puede tener varios cerebros; este cubre un solo propósito.
3. **Método**: presenta los presets de `sistema/presets/` con la línea "Úsalo si" de cada uno y
   recomienda uno según la respuesta anterior.

   | Preset | Archivo |
   |---|---|
   | PARA | `sistema/presets/para.md` |
   | Zettelkasten | `sistema/presets/zettelkasten.md` |
   | Espacios | `sistema/presets/espacios.md` |
   | Libre | `sistema/presets/libre.md` |

4. **Unidades iniciales** (opcional): lo que el preset elegido indique en su sección "Preguntas del
   bootstrap". Se puede saltar y crear después con el flujo `nuevo`.
5. **Versionado**: si la carpeta no es un repositorio git y git está instalado, pregunta si quiere
   inicializarlo. Explica que sirve para tener historial y poder deshacer.

## Confirmar

Muestra un resumen de lo que vas a crear: perfil, método, carpetas y unidades. Espera un sí.

## Escribir

1. `perfil.md` en la raíz, a partir de `sistema/plantillas/perfil.md`, con las respuestas 1 y 2.
2. `mapa.md`: reemplázalo completo por el bloque "Mapa" del preset elegido.
3. Las carpetas de la sección "Estructura" del preset. Agrega un `.gitkeep` a las que queden vacías.
4. Las unidades iniciales, siguiendo `sistema/flujos/nuevo.md` sin volver a pedir confirmación por
   cada una. Deja las plantillas con su estructura vacía: el contenido lo aporta la persona.
5. Si aceptó git: `git init`, `git add .` y un commit `Cerebro inicial`. No hagas `push`.

No borres `sistema/presets/`: sirve de referencia si después se quiere cambiar de método.

## Cierre

Muestra qué quedó creado y estos primeros pasos:

- Guardar lo primero que tenga en la cabeza: "captura …"
- Ordenarlo cuando tenga cinco minutos: "procesa el inbox"
- Al terminar de trabajar: "cierra la sesión"
