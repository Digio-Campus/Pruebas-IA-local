# Metodología de Pruebas de IA

Este documento detalla la metodología utilizada para evaluar diferentes modelos de Inteligencia Artificial en este proyecto.

## 1. Pruebas de Resumen (Summarization)

Para esta evaluación se utilizó un enfoque sistemático:
- Se proporcionó a cada modelo el mismo prompt: "summarize the following text"
- Se adjuntó el mismo texto original para todos los modelos
- La evaluación de calidad se realizó mediante un proceso de meta-evaluación automatizada:
  - Un modelo LLM evaluador recibió tanto el texto original como el resumen generado
  - Este evaluador asignó una calificación numérica y proporcionó un comentario cualitativo sobre la calidad del resumen
  - Se consideraron factores como precisión, concisión y retención de información clave

## 2. Pruebas de Detección de Ámbito (Domain Classification)

Esta evaluación midió la capacidad del modelo para identificar correctamente categorías temáticas:
- Se presentaron series de entradas cortas a cada modelo
- La tarea consistía en identificar el ámbito o categoría correspondiente a cada entrada
- Se empleó el mismo proceso de meta-evaluación:
  - Un LLM evaluador comparó la entrada original con la categorización realizada
  - Se asignaron calificaciones basadas en la precisión de la clasificación
  - Se proporcionaron comentarios cualitativos sobre el rendimiento

## 3. Pruebas de Protocolo de Contexto de Modelo (MCP)

Estas evaluaciones fueron de naturaleza cualitativa y manual:
- Se proporcionaron prompts específicamente diseñados para obligar al modelo a utilizar diferentes herramientas
- Se evaluó la capacidad del modelo para:
  - Reconocer cuándo se necesitaba una herramienta específica
  - Seleccionar la herramienta correcta para la tarea
  - Utilizar la herramienta de manera efectiva
  - Interpretar y aplicar correctamente los resultados obtenidos
- La evaluación se realizó cualitativamente mediante observación directa del rendimiento
