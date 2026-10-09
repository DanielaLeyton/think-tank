# Nuevo

Crea una unidad nueva en uno de los contenedores de `mapa.md`.

1. Lee la tabla "Contenedores" de `mapa.md` y las reglas que el mapa tenga para ese contenedor.
2. Determina el contenedor. Si el pedido no lo deja claro, pregunta mostrando las opciones con la
   descripción de cada una.
3. Define dos cosas a partir de lo que dijo la persona:
   - El **título**, en prosa normal: "Sitio web", "Recuperar información la fortalece más que
     releerla".
   - El **nombre de archivo o carpeta**: el título en `kebab-case`, sin tildes ni espacios.

   Si ya existe una unidad con ese nombre en ese contenedor, avisa y no la sobrescribas.
4. Crea la unidad según la columna "Unidad" del contenedor:
   - **Carpeta**: crea la carpeta y copia dentro los archivos de la columna "Plantilla".
   - **Archivo**: crea un solo archivo desde la plantilla indicada.
5. Reemplaza `{{nombre}}` por el título y `{{fecha}}` por la fecha de hoy. Completa lo que la persona
   haya dicho y aplica las reglas del mapa para ese contenedor; lo demás queda vacío.
6. Muestra qué se creó. Si el contenedor tiene `foco: sí`, pregunta si quiere enfocarse en esa
   unidad ahora.

Antes del paso 4, muestra qué vas a crear y dónde, y espera confirmación.
