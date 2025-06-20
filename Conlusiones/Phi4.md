## Phi4 mini

Es algo más lento que los otros modelos vistos hasta ahora.

Su evaluación con respecto a los 3 tipos de funcionalidad queda como sigue: 
- [Resumen: 0.86](#resumen) 
- [Ámbito: 0.75](#ámbito)
- [MCP: 0.45](#mcp) 

### Resumen 

| \   | Texto Largo   | Texto Corto   | Texto Medio       |
|-----------|-----------|-----------|-----------|
| **Nota**          |    0.90       | 0.85     | 0.85    |
| **Comentario**    | Muy buen resumen, con excelente cobertura normativa y conceptual, solo con leves omisiones estructurales.    | Muy buen resumen con enfoque periodístico, solo ligeramente afectado por tono informal y alguna interpretación libre.   | Resumen técnico sólido, con buena cobertura y estructura clara. Sólo pierde puntuación por omitir cifras clave y por usar una terminología un poco menos precisa   |

<br> 

### Ámbito 

| \     | Técnico  | Descripción médica   | Texto común  | Novela |
|-----------|-----------|-----------|-----------| -----------   |
| **Nota**          |       1       |   0.8   |   0.50    | 0.8     |
| **Comentario**    |      Reconoce correctamente el contexto técnico y el tipo de tareas asociadas. Inferencia bien razonada, específica y sin errores.       |   La inferencia principal es correcta, pero agrega una rama diagnóstica inexacta.   |    Reconoce que se trata pero  se dispersa en múltiples supuestos    | El modelo infiere correctamente el género principal pero se dispersa con géneros alternativos como “misterio”, “aventura” o “supervivencia” sin que el texto justifique esos caminos.    |


### MCP 

Es siempre la parte más frustrante de la prueba, pues muchas veces hay que cambiar de chat para que realice acciones de distinta manera a las que estaba haciendo. 

Además,  muchas veces da fallos por tonterías distintas sin ningún criterio de porque da un fallo u otro o funciona correctamente . 

Aunque el formateo correcto es: "params": { "timestamp": 1749807596.4 }  

Escribe de las siguientes formas:  

    - "params": "{timestamp: \"1749812396.9290798\"}"
    - "params": "{timestamp: 1749811128.6814387}",
    - E incluso, a veces, no introduce parámetro ninguno   


- Fecha y Hora: 
   - A veces no quiere llamar y dice que no puede
   - A veces llama bien a getTime, pero luego no sabe hacer bien la llamada a readableTime
        - O no pone parámetros
        - O no sabe formatear el json
        - O no sabe formatear el argumento 
        - Tras indicaciones puede realizar la llamada correctamente o no
   - A veces llama a getTime pero no a readableTime
   - A veces empieza a responder de manera desorbitada
   - Puede tener una restricción para el tiempo: 
        - Cuando detecta que es después de Marzo de 2023 que es cuando se entrenó 

- Noticias -> What are today's news: 
    - Parece completamente capado
    - No hace intento de llamar en ningún momento a la tool de búsqueda 
    - Genera todo el rato noticias simuladas

</br>