# Revisar

Audita que el contenido coincida con `mapa.md`. Lee todo el cerebro y es de solo lectura hasta que
la persona apruebe cada acción.

Revisa y reporta:

1. **Unidades incompletas**: unidades de tipo Carpeta a las que les falta un archivo de su plantilla.
2. **Contenido fuera del mapa**: carpetas o archivos de la raíz que ningún contenedor declara. No
   cuentan `sistema/`, `.claude/` ni los archivos base que lista `AGENTS.md`.
3. **Unidades inactivas**: sin cambios en más de 60 días en un contenedor con `archivar: sí`. Usa la
   última entrada de la bitácora o, si no hay, la fecha `creada`.
4. **Inbox estancado**: ítems con más de 14 días.
5. **Tareas vencidas**: cuántas y en qué unidades.
6. Lo que el mapa indique en su sección "Revisión".

Una unidad creada hace menos de 14 días no se reporta por estar vacía o sin actividad.

Presenta solo los hallazgos, como una lista numerada de acciones propuestas; lo que está en orden se
resume en una línea. La persona elige cuáles aplicar. Archivar es mover al contenedor de archivo del
mapa; nunca se borra nada.
