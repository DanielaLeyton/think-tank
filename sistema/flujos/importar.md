# Importar

Trae notas que la persona ya tiene en otro lugar y las ubica según `mapa.md`. Sirve para una carpeta
exportada de Notion, una bóveda de Obsidian, notas de Apple Notes o documentos sueltos.

El origen nunca se modifica ni se borra: se lee y se copia. El contenido se importa tal como está,
sin resumirlo ni reescribirlo.

## 1. Origen

Si la persona no dio la ruta de la carpeta o de los archivos, pídela. Si está fuera del cerebro y no
puedes leerla, pídele que la copie dentro, en una carpeta `importar/`.

## 2. Inventario

Lista los archivos del origen sin abrirlos y muestra un resumen:

- Cuántos son importables: texto en `.md`, `.txt`, `.html`, `.csv` o `.json`.
- Cuántos no lo son (imágenes, PDF, audio y otros) y cuáles.
- Cuántos ya fueron importados antes: su ruta aparece en un campo `importada-de:` de algún archivo
  del cerebro. Esos se omiten.

## 3. Plan

Lee `mapa.md`. Abre una muestra de hasta diez archivos, variada entre carpetas, y propón un plan en
una tabla, agrupando por carpeta o tema del origen:

| Grupo del origen | Archivos | Destino en el cerebro | Tipo |
|---|---|---|---|

- El destino es un contenedor y, si corresponde, una unidad del mapa. El tipo es uno de la tabla
  "Enrutamiento".
- Si un grupo necesita una unidad que no existe, proponla como nueva.
- Si ningún contenedor del mapa calza con un grupo, propón agregar uno. El mapa se cambia primero.
- Lo que no sepas ubicar va en una fila "Sin destino": no se importa y se lista al final.

Marca como inferencia lo que dedujiste de los nombres sin haber abierto los archivos. Espera
confirmación; la persona puede cambiar destinos o dejar grupos fuera.

## 4. Importar

Aplica el plan aprobado sin volver a preguntar por cada archivo. Si son más de veinte, avanza por
grupos e informa al terminar cada uno.

Para cada archivo:

1. Crea las unidades nuevas del plan con los pasos 3 a 5 de `sistema/flujos/nuevo.md`.
2. Escribe el contenido en su destino:
   - **Contenedor de unidad Archivo**: un archivo nuevo desde la plantilla del contenedor, con el
     texto original como cuerpo.
   - **Unidad de tipo Carpeta**: un archivo nuevo dentro de la carpeta de la unidad, con el texto
     original. No lo repartas entre los archivos de la plantilla.
3. Agrega al encabezado del archivo `importada-de: <ruta original>`. En `creada:` va la fecha del
   original si la tenía; si no, la de hoy.
4. Nombra el archivo en `kebab-case`, sin los códigos que agregan las exportaciones al nombre.
5. Si ya existe un archivo con ese nombre, no lo sobrescribas: agrega un sufijo y avisa.
6. Convierte los enlaces entre notas al formato del cerebro cuando el destino del enlace también se
   importó. Los demás quedan como texto.

Además:

- Las casillas `- [ ]` abiertas que encuentres se listan aparte, con su archivo de origen, para que
  la persona decida cuáles pasan a tareas. No las muevas por tu cuenta.
- Si una regla del mapa exige reescribir el contenido, como "una idea por nota", importa el original
  completo y anota la división como propuesta en el informe.

## 5. Informe

Termina con:

- Cuántos archivos se importaron y a qué destinos.
- Unidades y contenedores creados.
- Lo que quedó fuera: no importables, sin destino y omitidos por ya estar importados.
- Las tareas encontradas, para decidir cuáles se agregan.
- Las propuestas pendientes, como notas que conviene dividir.

Recuerda que el origen sigue intacto y que puede borrarlo cuando haya revisado el resultado.
