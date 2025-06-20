# Análisis Modelos Granite3

## Índice

- [Granite3.1-dense Desglose](#granite31-dense-desglose)
- [Granite3.1-moe Desglose](#granite31-moe-desglose)
- [Granite3.2-vision Desglose](#granite32-vision-desglose)

---

Resultado numérico final, con enlace a los distintos desgloses. 

| Modelo    | Resumen   | Ámbito    | MCP       |  Vision |
|-----------|-----------|-----------|-----------| ------- |
| granite3.1-dense        |    [0.73](#resumen-g31-d) | [0.975](#ámbito-g31-d)  | [0.4](#mcp-g31-d)    | - |
| granite3.1-moe          | [0.83](#resumen-g31-m)    | [0.95](#ámbito-g31-m)    | [0.2](#mcp-g31-m)    | - |
| granite3.2-vision       | [0.65](#resumen-g32-v)   | [0.625](#ámbito-g32-v)   | [0](#mcp-g32-v)   | [0.4](#vision) |

---

</br>

## Granite3.1-dense Desglose

### Resumen G31-D

| Media     | Texto Largo   | Texto Corto   | Texto Medio       |
|-----------|-----------|-----------|-----------|
| **Nota**          |    0.70       | 0.90     | 0.60    |
| **Comentario**    | Resumen es claro y ordenado, podría ajustar matices de terminología y agregar breves referencias normativas sin perder concisión.    | Resumen muy sólido, con omisiones deliberadas y adecuadas para este nivel de condensación.    | Resumen bien estructurado y comprensible, pero comete errores relevantes: atribuye efectos al gel que solo produce el ungüento y omite datos clave de variación esférica. Buena forma, precisión mejorable.   |

<br> 

### Ámbito G31-D

| Media     | Técnico  | Descripción médica   | Texto común  | Novela |
|-----------|-----------|-----------|-----------| ----------- |
| **Nota**          |    1       | 1    | 0.90    | 1 |
| **Comentario**    | El modelo identifica correctamente el dominio general: aprendizaje profundo (deep learning) y, más concretamente, tecnologías basadas en Transformers. Además, proporciona dos contextos válidos en los que estos modelos se utilizan frecuentemente   | El modelo identifica correctamente el ámbito profesional: medicina, con una precisión adicional al ubicarlo dentro de la clínica médica o atención sanitaria directa.   | Excelente razonamiento técnico, pero con una ligera suposición implícita sobre el tipo exacto de producto.   | El modelo interpreta con precisión el tono y los elementos del fragmento, inferencia muy bien fundamentada y sin suposiciones innecesarias. |


### MCP G31-D

- Hora: 
   - Primero ha devuelto una hora aleatoria, simulando las llamadas a la tool. 
   - luego ha llamado a las funciones "bien", añade un timestamp en la primera que se inventa 
   - Luego por alguna razón no sabe procesar la respuesta de readableTime y se queda haciendo llamadas en bucle
   - Una hipótesis plausible de esta MCP es que mis descripciones son muy cortas  

- Noticias -> What are today's news: 
    - Primero se las inventan y dice que es un asistente y es hipotético lo que genera
    - luego detecta la tool y la usa, pero con una url inventada, tras indicarle la URl lo ha usado bien. 
    - Ha Comentando varias noticias de actualidad, pero ha repetido varias veces, y no ha dado un resumen conciso. Le cuesta procesar tanto información.  
    - Cuando me han dado fallos los otros he vuelto, y ahora se niega también a buscar por internet

</br>

## Granite3.1-moe Desglose

### Resumen G31-M

| Media     | Texto Largo   | Texto Corto   | Texto Medio       |
|-----------|-----------|-----------|-----------|
| **Nota**          |    0.85       | 0.90     | 0.90    |
| **Comentario**    | En conjunto, es un resumen claro y muy completo, con solo pequeños matices de detalle normativo que podrían añadirse sin sacrificar concisión.    | En conjunto, aunque se podría ajustar ese detalle léxico, el resumen mantiene toda la información relevante sin resultar demasiado extenso.    | Resumen claro, bien estructurado y cubre prácticamente todos los elementos clave del estudio original, es técnicamente sólido, mantiene las cifras clave y refleja bien la metodología y los hallazgos. .   |

<br> 

### Ámbito G31-M

| Media     | Técnico  | Descripción médica   | Texto común  | Novela |
|-----------|-----------|-----------|-----------| ----------- |
| **Nota**          |    1       | 1    | 1    | 0.8 |
| **Comentario**    |Excelente nivel de detalle y contexto, menciona tareas concretas y arquitecturas (BERT, RoBERTa), enriqueciendo la inferencia.   |Preciso y bien enfocado, acierta en ubicarlo en medicina clínica y añade la especialización adecuada (gastroenterología/hepatología) coherente con el contexto.   | Respuesta muy afinada: identifica correctamente neumáticos de ciclismo de alto rendimiento para lluvia y alta velocidad, con justificación técnica y comparación con alternativas.   | Reconoce el tono  y asocia correctamente el fragmento a géneros de ficción especulativa.Pero, introduce elementos sin base en el texto, asumiendo supuestos más allá de las pistas dadas. |


### MCP G31-M

- Hora: 
   
   - Directamente ha reconocido y sabido que tenia que llamar a las tools
   - Sin embargo, no sabe introducir bien los argumentos en la llamada, ni ponerlos vacíos para pedir el tiempo, ni como introducir el float devuelto para pasarlo a legible. Se lo he tenido que indicar a mano.  
   
- Noticias -> What are today's news: 
    - Se las ha inventado y ni si quiera indica que es falso lo que genera
    - Parece que se niega ahora a usar la de buscar en internet
    


</br>

## Granite3.2-vision Desglose

### Resumen G32-V

| Media     | Texto Largo   | Texto Corto   | Texto Medio       |
|-----------|-----------|-----------|-----------|
| **Nota**          |    0.55       | 0.65     | 0.75    |
| **Comentario**    | Pierde demasiados matices estructurales y resulta menos informativo que los otros resúmenes evaluados.    |En conjunto, es comprensible, pero su brevedad e imprecisiones le restan fidelidad y exhaustividad.    | El resumen es claro y organizado, pero introduce conclusiones incorrectas y una interpretación añadida no respaldada por el texto.  |

<br> 

### Ámbito G32-V

| Media     | Técnico  | Decripcción médica   | Texto común  | Novela |
|-----------|-----------|-----------|-----------| ----------- |
| **Nota**          |    1       | 0.7   | 0.20    | 0.6 |
| **Comentario**    | Muy conciso y preciso, identifica correctamente NLP con justificación técnica, ideal para respuestas rápidas.  | Demasiado amplio y con generalizaciones (hematología, cardiología, cuidados críticos) que no se deducen del prompt; extiende innecesariamente el alcance del caso.   | Se desvía al proponer calzado deportivo, un producto distinto que no encaja con “combinación que permite montar a alta velocidad sin patinar”. La inferencia no refleja el contexto de “ride” en vehículos.   | Acierta al situarlo en un ámbito de ficción especulativa (fantasy) o misterio, pero incluye “crime fiction” sin justificación clara en el texto. Es demasiado genérico y disperso, perdiendo precisión al no centrarse en el tono gótico/terrorífico visible. |


### MCP G32-V

- Hora: 
   - Me ha dicho que no puede usar MCP tools, no se como de cierto es, pero lo ha dicho.
   - Desde luego que parece empeñado en no usarlas

- Noticias -> What are today's news: 
    - Se las ha inventado y ni si quiera indica que es falso lo que genera
    - Parace que se niega ahora a usar la de buscar en internet


### Vision

Es bastante bueno en reconocimiento de patrones, numero de objetos de un tipo que hay en una imagen, y lo hace bastante rápido.

- Si aparecen objetos por el fondo y pequeños ya le cuesta mas identificarlos

- He probado a que me diga edad de personas en la foto, pero no quiere hacerlo diciendo que no es ético. 

Sin embargo, aunque reconoce, las cosas mas complicadas que requieren un análisis complejo le cuestan más:
    
- He puesto una imagen de un frente de la guerra, y se ha quedado estancado en una etiqueta del mapa, sin darle importancia al resto de la imagen.

- He puesto un mapa conceptual que explicaba los grafos, y pedido que me lo explicará, y ha intentado pasarlo a texto y ya.

- He puesto una foto de google maps de una salida de la autovía, se ha inventado el numero de la salida y no lee bien los carteles

En conclusion, el modelo es decente, pero tiene mucha capacidad de mejorar. Las cosas más básicas las realiza bien, pero cálculos más complejos le cuestan. 
