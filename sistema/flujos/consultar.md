# Consultar

Responde una pregunta con lo que el cerebro tiene guardado, citando de dónde sale cada dato. Aplica
cuando la persona pregunta por algo suyo: "¿qué decidimos sobre…?", "¿qué sé de…?", "¿dónde anoté…?",
"¿cuándo fue…?".

Este flujo solo lee. No escribe nada.

## 1. Alcance

Busca en todo el contenido del cerebro, incluido el contenedor de archivo. No busques en `sistema/`,
`.claude/` ni en los archivos de instrucciones.

Si `mapa.md` tiene una regla de aislamiento y hay un foco activo, busca solo dentro de ese foco, dilo
en la respuesta y ofrece ampliar la búsqueda si la persona lo pide.

## 2. Buscar

1. Saca de la pregunta los términos clave y agrega sinónimos y variantes: singular y plural, con y
   sin tilde, nombres propios relacionados.
2. Busca esos términos en los archivos del alcance. Mira también los nombres de archivos y carpetas.
3. Abre solo los archivos con coincidencias y lee la sección que rodea a cada una.
4. Si no aparece nada, intenta una vez más con términos más generales antes de darte por vencido.

## 3. Responder

- Empieza por la respuesta, en una o dos frases.
- Cada dato lleva su origen: la ruta del archivo y la sección, y la fecha si el dato la tiene.
- Usa las palabras de la persona. Cita textual cuando el matiz importe.
- Si hay datos que se contradicen, muestra ambos con sus fechas y di cuál es el más reciente. No
  elijas uno en silencio.
- Si la respuesta está incompleta, di qué parte falta.

Responde solo con lo que está guardado. Si agregas algo que sabes por tu cuenta, ponlo aparte, bajo
"Fuera de tu cerebro", para que no se confunda con lo suyo.

## 4. Si no hay nada

Dilo sin rodeos, cuenta con qué términos buscaste y ofrece capturar la pregunta al inbox. No
respondas con conocimiento general como si viniera del cerebro.
