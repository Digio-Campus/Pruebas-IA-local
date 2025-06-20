# Metodología de Pruebas de IA

Este documento detalla la metodología utilizada para evaluar diferentes modelos de Inteligencia Artificial en este proyecto.

Los modelos se han probado de manera local usando el motor de [ollama](https://ollama.com/) y el cliente de modelos de lenguaje [Cherry Studio](https://github.com/CherryHQ/cherry-studio).

## 1. Pruebas de Resumen (Summarization)

Esta evaluación midió la capacidad del modelo para analizar y resumir correctamente un texto, para ello se utilizó un enfoque sistemático:

- Se proporcionó a cada modelo el mismo prompt: "summarize the following text: \\n *El texto en particular*"
- Los textos en concreto se encuentran en la carpeta [Recursos/Textos](/Recursos/Textos/). 
- La evaluación de calidad se realizó mediante un proceso de meta-evaluación automatizada:
  - Un modelo LLM evaluador recibió tanto el texto original como el resumen generado
  - Este evaluador asignó una calificación numérica y proporcionó un comentario cualitativo sobre la calidad del resumen
  - Para afinar más en la evaluación, tras realizar las primeras evaluaciones, se creo una conversación por tipo de texto:
    - [Texto Largo](https://github.com/copilot/share/c06d0286-4844-8cc3-b902-c042e0410920)
    - [Texto Medio](https://github.com/copilot/share/42455314-0860-8865-8902-d242e4cb6070)
    - [Texto Científico](https://github.com/copilot/share/c2650214-0940-8ce5-9050-4003e0c30861)
    - [Texto Periodístico](https://github.com/copilot/share/404c0184-0060-88e1-b942-5043c44b0061)  
  
  - En estos chats con introducir una salida es suficiente para obtener la evaluación buscada.
  - Se recomienda periódicamente introducir el siguiente prompt:
    - "Con las evaluaciones hasta este momento, consideras que se debe reajustar la escala, o ves bien las notas dadas"
- Finalmente, los resultados y comentarios adicionales pertinentes se documentaron en los distintos archivos dedicados a cada modelo. 
  
## 2. Pruebas de Detección de Ámbito (Domain Classification)

Esta evaluación midió la capacidad del modelo para identificar correctamente categorías temáticas, para ello se utilizó un enfoque sistemático similar al anterior:

- Se proporcionó a cada modelo el mismo prompt: "Responde a la siguiente batería de test:: \\n *Los tests*"
- La batería usada se encuentra disponible en [ámbito.md](/Recursos/Ambito.md)
- Se empleó el mismo proceso de meta-evaluación:
  - Un LLM evaluador comparó la entrada original con la categorización realizada
  - Este asignó una calificación y comentario basándose en la precisión de la clasificación
  - Al igual que en el caso anterior se creo un [chat](https://github.com/copilot/share/c86d1394-4840-8041-9902-d20ac0814922) particular para realizar este proceso automáticamente. 
  - En este chat basta con introducir la salida a la batería para obtener la evaluación del LLM. 

## 3. Pruebas de Protocolo de Contexto de Modelo (MCP)

Estas evaluaciones fueron de naturaleza cualitativa y manual:
- Los servidores MCPs usados se exponen en los [recursos](/Recursos/README.md)
- Se proporcionaron prompts específicamente diseñados para obligar al modelo a utilizar diferentes herramientas, algunos ejemplos son:
  - que dia es? 
  - que hora es?
  - dime los últimos resultados de f1
  - que dice la pagina principal de wikipedia
  - Que archivos tengo en mi carpeta de descargas
  - Que dice el *archivo.pdf* que tengo en mi carpeta de descargas 

- Se evaluó la capacidad del modelo para:
  - Reconocer cuándo se necesitaba una herramienta específica
  - Seleccionar la herramienta correcta para la tarea
  - Utilizar la herramienta de manera efectiva
    - Sobretodo realizar las llamadas correctamente 
  - Interpretar y aplicar correctamente los resultados obtenidos
  - Encadenar herramientas cuando es necesario 

- La evaluación se realizó cualitativamente mediante observación directa del rendimiento
- En caso de errores se probo a modificar el prompt del agente para intentar obtener mejores resultados. 
