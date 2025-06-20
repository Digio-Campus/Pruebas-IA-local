# Hermes3

Evaluación con respecto a los 3 tipos de funcionalidad probadas: 
- [Resumen: 0.81](#resumen) 
- [Ámbito: 0.9](#ámbito)
- [MCP: 0.05](#mcp) 

En conclusión, a nivel textual, es una mezcla entre el 1.7b y el 4b, pero no compensa con respecto al 1.7b. Y lo más importante no soporta bien los MCPs. 

### Resumen 

| Media     | Texto Largo   | Texto Medio   | Texto Periodístico | Texto Científico
|-----------|-----------|-----------|-----------|-----------|
| **Nota**          |   0.84     | 0.86     | 0.8 | 0.75 |
| **Comentario**    | Muy buen resumen, con cobertura casi completa y solo falta mencionar algunos detalles de la composición de los reales y matizar algunos puntos de los axiomas.  | Resumen es claro, fiel al texto original y cubre casi todos los puntos clave, se pierden algunos matices en la descripción de la “dualidad de escalas” y la mención explícita de los niveles de competencia (1, 2, 3), pero es muy completo y bien organizado      | Resumen detallado y bien estructurado, cubre actores principales. Sin embargo, es demasiado extenso, incluye interpretaciones y matices especulativos.  | Resumen es detallado y bien estructurado. Sin embargo, comete dos errores de interpretación relevantes. En conclusión,  buena forma, pero precisión y fidelidad mejorables. |

**Comentarios personales**
- Texto medio: Como forma de escribir me gusta más, menos esquemático mas textual
- Texto largo: Igual que el medio mas textual que los primeros.
- Texto Periodístico: Mas que resumir ha extendido el texto y ha incluido suposiciones bastante flojo
- TExto científico: Copilot habla de errores de precisión, a nivel estructural el mejor. 


<br> 

### Ámbito 

He introducido una batería de 30 test generados por Gemini. 

**Comentarios Copilot**

El modelo destaca en precisión de ámbito temático, con respuestas claras, breves y correctas en el 90% de los casos. Su formato de “etiqueta + aclaración” es muy útil para tareas de clasificación o etiquetado automático.

- Este modelo es excelente para clasificación temática rápida y precisa.
- Sus puntos débiles son la falta de estandarización total de etiquetas y la ocasional falta de matiz, pero no comete errores graves ni repite respuestas.
- Ideal para sistemas donde se requiera una respuesta tipo “etiqueta” o para alimentar modelos de clasificación automática.
- Si se quiere usar en español o para usuarios no expertos, convendría adaptar las etiquetas a una taxonomía consensuada en el idioma y ámbito de aplicación.

**Comentario Personal:**
- Se le puede introducir la batería entera sin problemas
- El que más rápido ha respondido de los 3
- Ha respondido en ingles a pesar de que la entrada ha sido en español
- La estructura de las respuestas es bastante distinta de la de los otros dos modelos que han respondido a toda la batería, aun asi es la que más me ha gustado, concisa y legible 
- La corrección de las respuestas se la he dejado a copilot


### MCP 

En general, no llama. 

- Tiempo: 
   - Simula las llamadas a los MCPs pero no llama

- Búsqueda internet : 
    - No hace intento de llamar en ningún momento a la tool de búsqueda 
    - Genera todo el rato noticias simuladas

- Sistema de ficheros
    - Simula que llama a listar

- PDF -> MD
    - Se ha inventado los argumentos
    - Pero ha realizado la llamada

</br>