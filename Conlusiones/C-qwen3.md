# Análisis Modelos qwen3

## Índice

- [qwen3-0.6b](#qwen3-06b-desglose)
- [qwen3-1.7b](#qwen3-17b-desglose)
- [qwen3-4b](#qwen3-4b-desglose)

---

Resultado numérico final, con enlace a los distintos desgloses. 

| Modelo    | Resumen   |   Ámbito   | MCP       |  
|-----------|-----------|-----------|-----------| 
| qwen3-0.6b      |  [0.8](#resumen-06b) | [0.5 = 0.7-0.2](#ámbito-06b)   | [0.3](#mcp-06b)   | 
| qwen3-1.7b      |  [0.90](#resumen-17b) | [0.85](#ámbito-17b)    | [0.5](#mcp-17b)   | 
| qwen3-4b        | [0.88](#resumen-4b)  | [0.9](#ámbito-4b)   | [0.6](#mcp-4b)     | 


Resultados finales
- El **modelo 0.6b**: buen modelo de procesado de lenguaje, rápido y capaz, es peor en reglas generales que los otros 2 modelos como era de esperar, pero se defiende bien. 
    - Mayores inconvenientes: procesado de prompts multi-pregunta y MCPs.  
- El **modelo 1.7b**: calidad/tamaño el mejor.
    - Mayores inconvenientes: Peor en temas más específicos, y algo peor en MCPs
- El **modelo 4b**: El mejor de los 3, con fallos obviamente, pero cubre lo que los otros no
    - Mayores inconvenientes: Sigue teniendo problemas con MCPs y no despunta tanto con respecto al 1.7b
---

</br>

## qwen3-0.6b Desglose

### Resumen 0.6b

| Media     | Texto Largo   | Texto Medio   | Texto Periodístico | Texto Científico
|-----------|-----------|-----------|-----------|-----------|
| **Nota**          |   0.8      | 0.78     | 0.9 | 0.70 |
| **Comentario**    | Resumen estructurado y claro de las secciones principales del texto. Sin embargo, hay algunos errores conceptuales y omite detalles importantes | Resumen claro, estructurado y que cubre la mayoría de los puntos esenciales. Sin embargo, pierde algunos matices de detalle y la vinculación normativa no es tan precisa. La síntesis final es correcta pero algo general.   |  Es fiel al original y condensado adecuadamente. Le falta solo un matiz menor, pero no distorsiona el mensaje principal. Muy sólido.   | Resumen es claro y bien organizado, pero presenta errores de precisión importantes |

**Comentario personales**
- Largo y medio: No maneja tanto el texto pero lo procesa bien y lo esquematiza
- Periodístico: lo hace textual y conciso.
- Científico: Al igual que 1.7 vuelve a ser esquemático y aquí le acusa gravemente de no procesar bien el texto. 

En conclusión, es peor en general, aunque se defiendo bien en temas generales. Ha perdido precision en derecho y medicina, ya en lo concreto. 


<br> 

### Ámbito 0.6b

He introducido una batería de 30 test generados por Gemini. 

He divido su nota Copilot le da un 0.7 pero no tiene en cuenta que no recibe toda la batería de una, lo cual me parece muy deficiente. 

**Comentarios Copilot**

El modelo acierta en la mayoría de temas generales pero tiene problemas importantes de dispersión y desconcierto en las categorías, sobre todo en los últimos tests. Presenta varios errores de “arrastre” y mezcla categorías irrelevantes. Su redacción es menos precisa que la de los otros modelos analizados.

- El modelo es capaz de captar el tema general de la mayoría de textos, pero falla notablemente en la categorización precisa y en la formulación de ámbitos estándar.
- Presenta problemas de repetición y arrastre en los últimos tests, lo que reduce la fiabilidad en baterías largas.
- Su estilo es redundante y menos profesional comparado con los otros modelos.
- Puede servir para una clasificación temática muy general, pero no para tareas donde la precisión y la estandarización de categorías sea clave.

**Comentario Personales**
- No procesa la batería entera bien, da una única respuesta, luego hay que introducirlos de uno en uno.
- Responde más rápido que ninguno, también porque es pregunta a pregunta
- Responde con frases demasiado cortas 
- La corrección de las respuestas se la he dejado a copilot


### MCP 0.6b

- Tiempo
    - A diferencia de otos pequeños si que llama al MCP
    - Sin embargo es mas inconsistente
        - Llama tanto a readable como a getTime de manera aleatoria en cada consulta
        - Pone bien los parámetros vacíos, pero en readable a veces escapa caracteres
    - No enlaza la llamada de getTime con la de readable 

- Búsqueda Internet
    - No llama en ningún caso al MCP

- Filesystem
    - Como los otros no maneja bien por sistema de ficheros
    - Al igual que el 1.7 no busca los disponibles 

- PDF
    - llama a move de file system en vez de a la tool




</br>

## qwen3-1.7b Desglose

### Resumen 1.7b

| Media     | Texto Largo   | Texto Medio   | Texto Periodístico | Texto Científico
|-----------|-----------|-----------|-----------|-----------|
| **Nota**          |   0.92      | 0.92     | 0.95 | 0.8 |
| **Comentario**    | Excelente síntesis, muy fiel al contenido y propósito del texto, con solo mínimos detalles omitidos.   | Resumen es muy completo, bien estructurado y recoge casi todos los matices importantes. Solo faltan detalles muy menores en la explicación de la dualidad de escalas y la vinculación exacta entre los grados y los niveles de competencia.   |  Muy fiel y preciso, solo se podría considerar mínimamente redundante en la reiteración de “historic agreement”, pero no afecta la calidad global. Muy completo y claro.   | Resumen claro, bien estructurado y recoge los puntos principales del estudio. Sin embargo, simplifica y generaliza algunos resultados. En conclusión, es fiel en lo esencial pero pierde precisión y detalle en los resultados. |

**Comentario personales**
- Largo y medio: Al igual que el 0.6b no maneja tanto el texto pero lo procesa bien y lo esquematiza
- Periodístico: Al igual que le 0.6b pasa a ser textual pero algo más extenso y completo. 
- Científico: vuelve a ser muy esquemático, copilot le acusa de perder detalle y precisión.

En conclusión, aunque es mas esquemático que textual, entiende muy bien la información y la procesa muy bien. Su mayor fallo ha sido en un tema ya muy técnico. 

<br> 

### Ámbito 1.7b

He introducido una batería de 30 test generados por Gemini. 

**Comentario Copilot:**
- El modelo comprende los temas, pero a veces categoriza de forma demasiado amplia o utiliza términos menos habituales.
- Comete algún error factual leve (OMS/ONU) y ocasionalmente mezcla ámbitos (“alimentación y consumismo”).
- Puede mejorar en la precisión de las etiquetas y en evitar redundancias.
- Es sólido para tareas generales de clasificación temática, aunque se recomienda ajustar la especificidad y estandarizar las categorías.

**Comentario Personal:**
- Se le puede introducir la batería entera sin problemas
- Responde más rápido que 4b
- Responde con frases cortas y una estructura legible
- La corrección de las respuestas se la he dejado a copilot


### MCP 1.7b

- Tiempo
    - Error de parámetro -> pone este formato "params": "\<result>17:55\</result>"
    - Tanto al pedir dia como hora, llama a readableTime sin llamar a getTime
    - Incluso al decir hoy en el prompt no llama a getTime  
    - Al igual que el 4b el poner el modo de think es peor para los MCPs
    - Y tampoco cambiar el prompt soluciona nada 

- Búsqueda internet 
    - Realiza las búsquedas mediante el MCP, pero a veces no del todo bien
    - A Wikipedia no llama
    - Resultados de f1, ha hecho la llamada bien pero no ha sabido procesar los datos

- Filesystem
    - No sabe manejarse por el sistema de ficheros
    - Indicando la ruta si que sabe actuar 

- Pdf-Md
    - Igual que el 4b

</br>

## qwen3-4b Desglose

### Resumen 4b

| Media     | Texto Largo   | Texto Medio   | Texto Periodístico | Texto Científico
|-----------|-----------|-----------|-----------|-----------|
| **Nota**          |   0.87    | 0.88     | 0.88 | 0.9 |
| **Comentario**    | Muy buen resumen general, con todos los puntos clave cubiertos y solo algunos detalles secundarios omitidos.   | Resumen claro, ordenado y que recoge los elementos normativos y estructurales principales. Solo le falta un poco más de precisión en la relación entre la dualidad de escalas y el catálogo nacional, y podría detallar un poco más sobre el rol de la certificación y la orientación profesional.    | resumen es claro, preciso y recoge todos los actores y hechos principales, falta matizar el beneficio explícito para los ciudadanos y no menciona la implicación positiva.   | Resumen es claro y fiel, cubre los métodos, resultados clave y conclusiones. Incluye las cifras más relevantes y no introduce errores ni interpretaciones añadidas. En general refleja bien la información esencial y mantiene precisión técnica. |

**Comentario personales**
- Largo y medio: A diferencia de los otros dos modelos hace los resúmenes mucho mas textuales.
- Periodístico: Es más conciso que el resto, buscando resumir más que transmitir toda la información
- Texto científico: muy conciso, pero según copilot muy completo.

<br> 

<br> 

### Ámbito 4b

He introducido una batería de 30 test generados por Gemini. 

**Comentario Copilot:**
- El modelo es muy fiable para identificar el ámbito/categoría principal de un texto informativo.
- Sus errores son mayormente de precisión fina o redundancia, no de comprensión.
- Destaca en la capacidad de ofrecer detalles relevantes y no omitir información clave.
- Solo necesita mejorar en la concreción (ser más directo y menos redundante) y evitar pequeños errores de factualidad (como confundir tenis con fútbol en el caso de Nadal).

**Comentario Personal:**
- Se le puede introducir la batería entera sin problemas
- Responde algo mas lento en comparación con el resto
- Responde con frases cortas y una estructura legible
- La corrección de las respuestas se la he dejado a copilot

### MCP 4b

- Tiempo
    - Vuelve a tener el error del parámetro vacío en getTime
    - Al pedir el dia no suele llamar a getTime sino que se inventa el timestamp
    - Al poner: "que dia es *hoy*" si que llama a getTime.
    - Ni indicando en el prompt que no reciba parámetros lo hace 
    - En modo think indica correctamente lo que tiene que hacer pero no lo hace

- Búsqueda internet 
    - Realiza las búsquedas mediante el MCP, pero a veces no del todo bien
    - A Wikipedia, llama bien sintácticamente, pero no semánticamente
        - Obtiene metadatos pero no información
    - he pedido que me diga los últimos resultados de f1 y ahi perfecto

- Filesystem
    - Al principio ha llamado mal pero se ha corregido y llamado a directorios permitidos 
    - Luego no sabe identificar que si le digo descargas es la ruta desde C: no desde cherry
    - No sabe manejarse por el sistema de ficheros

- Pdf to markdown
    - Si le indicas la ruta entonces lo hace bien



