# Procesar inbox

Lleva cada ítem de `inbox.md` a su destino según la tabla "Enrutamiento" de `mapa.md`.

1. Lee `inbox.md` y `mapa.md`. Si el inbox está vacío, dilo y termina.
2. Para cada ítem, de a uno, propón:
   - **Tipo**: uno de los tipos de la tabla "Enrutamiento". Si el ítem mezcla varios (una idea y su
     fuente, una tarea y una decisión), propón dividirlo en partes, cada una con su tipo y destino.
   - **Destino**: la unidad y el archivo concretos. Para elegir la unidad, usa los nombres de las
     unidades existentes y la marca `(desde: …)` si la hay. Si lo deduces del texto, dilo.
   - **Texto final**: reescrito para que se entienda sin contexto, si hace falta. Una fecha límite
     mencionada en el texto pasa a `(vence: …)`.
3. La persona puede aceptar, cambiar el destino, editar el texto, descartar o saltar.
4. Al aceptar, escribe el ítem en su destino y elimina la línea del inbox:
   - En un archivo existente: con el formato que el mapa indica para ese tipo, al final de la
     sección que corresponda. Las tareas van al final de "Pendientes".
   - Si el destino es una unidad nueva: créala con los pasos 3 a 5 de `sistema/flujos/nuevo.md`.
5. Al descartar, elimina la línea. Al saltar, no toques nada.
6. Si ningún destino calza, ofrece crear una unidad nueva o dejarlo en el inbox.
7. Termina con un resumen: cuántos se movieron y adónde, cuántos se descartaron y cuántos quedan.

Si hay más de diez ítems, ofrece primero una propuesta en tabla para aprobar en bloque, y revisa de a
uno solo los que la persona marque.
