# Recursos para Pruebas de IA

Esta carpeta contiene los recursos utilizados para realizar las pruebas de los modelos de inteligencia artificial.

## Índice

- [Recursos Disponibles](#recursos-disponibles)
  - [Servidores MCP](#servidores-mcp)
  - [Archivo Ambito.md](#archivo-ambitomd)
    - [Batería principal](#batería-principal-de-pruebas)
    - [Pruebas adicionales](#pruebas-adicionales)
  - [Carpeta Textos](#carpeta-textos)
    - [Texto-Largo.md](#texto-largomd)
    - [Texto-Medio.md](#texto-mediomd)
    - [Texto-Científico.md](#texto-científicomd)
    - [Texto-Periodístico.md](#texto-periodísticomd)

## Recursos Disponibles

### Servidores MCP

Para las pruebas de capacidades MCP (Model Context Protocol) se han utilizado los siguientes servidores:

| Servidor MCP | Repositorio | Función |
|-------------|------------|---------|
| PDF a Markdown | [PDFtoMD-Converter](https://github.com/javilujann/PDFtoMD-Converter) | Conversión de archivos PDF a formato Markdown |
| Tiempo MCP | [TimeMCP](https://github.com/javilujann/TimeMCP) | Funciones relacionadas con el tiempo (timestamp y conversión) |
| Sistema de Archivos | [Filesystem Server](https://github.com/modelcontextprotocol/servers/tree/main/src/filesystem) | Manejo del sistema de ficheros |
| Búsqueda Web | [Exa Server](https://smithery.ai/server/exa) | Realización de búsquedas por internet |

Estos servidores MCP permiten evaluar la capacidad de los modelos para interactuar con herramientas externas y utilizar información contextual para resolver tareas específicas.


### Archivo [Ambito.md](Ambito.md)

Este archivo contiene una colección de pruebas diseñadas para evaluar la capacidad de los modelos de inteligencia artificial para identificar correctamente el ámbito o dominio temático de diferentes textos.

Las pruebas varían en longitud, complejidad y temática, permitiendo una evaluación integral de las capacidades de comprensión contextual de los modelos.

Se divide en dos secciones : 

- Batería principal de 30 pruebas generada por Gemini en la siguiente [conversación](https://g.co/gemini/share/ec8c6f98ab33). 
    
    - La corrección de la salida generada por una IA de estas pruebas se puede hacer de manera automática mediante Copilot como se indica en la [metodología](../METODOLOGIA.md).

-  Pruebas adicionales que se usaron inicialmente para probar los modelos más pequeños, previo a la automatización y creación de la batería de pruebas anteriores. 
    - Generadas por ChatGPT. 

### Carpeta Textos

Esta carpeta contiene los diversos textos utilizados como base para las pruebas de resumen de los modelos de IA:

#### Texto-Largo.md
Extracto de un libro de análisis matemático utilizado para evaluar la capacidad de los modelos para resumir textos técnicos de gran extensión. Este texto provee un buen ejemplo de contenido académico con terminología especializada y estructura formal.

Fuente: [Mathematical Analysis Second Edition - Apostol](https://www.google.com/search?q=mathematical+analysis+second+edition+apostol)

#### Texto-Medio.md
Texto normativo de carácter legal que describe un Real Decreto. Contiene lenguaje formal administrativo, referencias a artículos de leyes, y estructura jerárquica típica de los textos legislativos. Su extensión media lo hace ideal para evaluar cómo los modelos procesan y sintetizan documentación legal oficial.

Fuente: [Real Decreto 404/2025 - Boletín Oficial del Estado](https://www.boe.es/boe/dias/2025/06/12/pdfs/BOE-A-2025-11810.pdf)

#### Texto-Científico.md
Fragmento de un artículo médico relacionado con estudios clínicos. Sirve para evaluar la capacidad de los modelos para comprender y resumir información técnica en el ámbito de la científico, con terminología específica y datos estadísticos.

Fuente: [Análisis de las alteraciones topográficas inducidas por distintos preparados de sustitutos de la lágrima](https://dialnet.unirioja.es/servlet/articulo?codigo=6767650)

#### Texto-Periodístico.md
Fragmento de artículo periodístico sobre temas de actualidad. Empleado para analizar cómo los modelos procesan información de registro menos formal y más narrativo, incluyendo hechos, citas y opiniones.

Fuente: [El Mundo: Acuerdo histórico sobre Gibraltar](https://www.elmundo.es/espana/2025/06/11/68496d33e4d4d8f77b8b45a1.html)