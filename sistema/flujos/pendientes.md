# Pendientes

Muestra las tareas abiertas sin cargar el resto del contenido.

1. Lee en `mapa.md` qué archivos contienen tareas (fila "Tarea" de "Enrutamiento"). Son solo esos:
   `inbox.md` y el contenedor de archivo no cuentan.
2. Alcance: el foco activo por defecto. Todo el cerebro si la persona lo pide, si no hay foco o si
   el mapa tiene un solo archivo de tareas.
3. Busca solo las líneas `- [ ]` de esos archivos. No abras los demás archivos de cada unidad.
4. Muestra las tareas agrupadas por unidad, omitiendo las unidades sin tareas. Dentro de cada grupo,
   primero las vencidas, luego las que tienen fecha en orden y al final las que no tienen.
5. Cierra con una línea de totales: abiertas, vencidas y cuántas vencen en los próximos siete días.

Formato de una tarea:

```
- [ ] Descripción (vence: AAAA-MM-DD)
- [x] Descripción (hecha: AAAA-MM-DD)
```

La fecha de vencimiento es opcional. Al completar una tarea, márcala y muévela a "Hechas".
