# Smollm2 Diferencias entre modelos
    
Todos los modelos responden rápidamente, sin embargo hay bastas diferencias entre ellos. Aunque hay fallos comunes entre ellos.
 
El principal: Todos se quedan "*estancados*" en el primer contexto o prompt recibido y aunque intentes cambiar de tema vuelven a relacionar lo nuevo con lo original. Hay que cerrarlo y volver a abrirlo 

## 135M

El más pequeño y, como cabía suponer, el peor. En particular destacar que a veces responde cosas sin sentido.  

 - Español

    Lo primero que he probado en todos, ha sido hablar en español, y aunque lo reconoce y de vez en cuando dice algo en español, este modelo ni responde ni analiza bien el español.

- Datos
    
    Otro prompt estándar ha sido preguntar datos históricos, en este caso, da una información poco técnica y más narrada, además me ha llegado a dar una fecha mal, 14 de Junio en vez de 6.

- Resumen
    
    Realiza un resumen, acortando el texto original mayoritariamente.


## 360M

El que más me ha sorprendido

 - Español

    Reconoce perfectamente el idioma y lo que le pides, pero no he conseguido que deje de responde en inglés. 

- Datos

    Da datos más exactos, en particular, con respecto a mi pregunta(el desembarco de normandía) ha dado nombre de operaciones y ha explicado la importancia. 

    Aunque sorprendentemente, en una interacción ha respondido diciendo que no podia darme información histórica.  

- Resumen

    Realiza un resumen correcto, con otras palabras y explicando algo los conceptos.


## 1.7B

Como era esperable el que mejor funciona 

 - Español

    Puedes hablar en español con el perfectamente.

- Datos

    Datos correctos, completos y en buena cantidad. Similar a la introducción de la pagina de Wikipedia.

- Resumen
    
    Ha sintetizado los conceptos y añadido algo nuevo. 

- MCP

    El único que llama pero se queda en un bucle, no se porque. 