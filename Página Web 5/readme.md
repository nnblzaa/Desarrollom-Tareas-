## Nombre del proyecto
Noticias climáticas del día
## Descripción
La actividad consistió en construir una página web que muestra un resumen de las noticias ambientales más recientes, explicado por inteligencia artificial. La persona elige un tema (por ejemplo, cambio climático o sequía Sinaloa) y presiona "Ver noticias"; la página envía el tema a un webhook de Make, donde un escenario llamado "Integration Webhooks, Make AI Agent" busca las noticias más recientes en Google News mediante RSS, las junta en un solo texto y un agente de IA las resume. La respuesta regresa a la página, que muestra el resumen con los enlaces a las fuentes originales.
## Objetivos de aprendizaje
Objetivo general. Construir, sin programar, una herramienta de difusión ambiental que obtenga noticias recientes mediante RSS, las resuma con inteligencia artificial y las muestre en una página web, verificando que los resúmenes sean fieles a sus fuentes.
Con esta actividad se aprendió a:
- Generar con IA una página web de un solo archivo HTML que envía datos a un webhook de Make.
- Conectar una página web con Make mediante un Custom webhook y recibir el tema elegido.
- Leer noticias recientes de Google News con el módulo RSS y unirlas con un Text aggregator para que la IA se ejecute una sola vez.
- Configurar un Make AI Agent con instrucciones claras para que resuma únicamente la información de las noticias recibidas.
- Devolver la respuesta a la página con un Webhook Response y publicar la página en GitHub Pages.
- Comparar los resúmenes de la IA con las noticias originales y reconocer los riesgos de difundir información sin verificarla.

## Resultados
[PDF](https://github.com/nnblzaa/Desarrollom-Tareas-/blob/main/P%C3%A1gina%20Web%205/Resultados/informe_practica_3_5%20(1).pdf)

## Material y herramientas utilizadas
- Make (plataforma de automatización en línea) para crear el escenario con sus módulos.
- Módulos de Make: Webhooks (Custom webhook), RSS (Retrieve RSS feed items), Tools (Text aggregator), Make AI Agent (Run an agent) y Webhooks (Webhook response).
- Make's AI Provider como conexión del agente de inteligencia artificial.
- Google News (feed RSS) como fuente de las noticias.
- IA generativa (versión gratuita) para generar el archivo index.html de la página.
- GitHub y GitHub Pages para alojar y publicar la página.
- Computadora con Windows, navegador web (Microsoft Edge) y conexión a internet




## Imagen
<img width="1600" height="1200" alt="image" src="https://github.com/user-attachments/assets/d0076ba5-70a6-4823-be24-3354b0c74491" />

<img width="1600" height="1200" alt="image" src="https://github.com/user-attachments/assets/995fef18-913b-451f-ac4c-36ba8133e4d8" />


## Video
[Video](https://youtube.com/shorts/nC4UmBKlh_A?si=mkAhSuSitssCLLQA)

## Codigo
[main.txt](./codigo/main.txt)
