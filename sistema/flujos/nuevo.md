# Nuevo

Crea una unidad nueva en uno de los contenedores de `mapa.md`.

1. Lee la tabla "Contenedores" de `mapa.md`.
2. Determina el contenedor. Si el pedido no lo deja claro, pregunta mostrando las opciones con la
   descripción de cada una.
3. Define el nombre en `kebab-case`, sin tildes ni espacios. Si ya existe una unidad con ese nombre
   en ese contenedor, avisa y no la sobrescribas.
4. Crea la unidad según la columna "Unidad" del contenedor:
   - **Carpeta**: crea la carpeta y copia dentro los archivos de la columna "Plantilla".
   - **Archivo**: crea un solo archivo desde la plantilla indicada.
5. Reemplaza `{{nombre}}` y `{{fecha}}` en lo copiado. Completa solo lo que la persona haya dicho; lo
   demás queda vacío.
6. Muestra qué se creó y pregunta si quiere enfocarse en esa unidad ahora.
