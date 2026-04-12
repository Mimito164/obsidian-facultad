---
fecha: 2026-03-27 2026-03-27
materia: Comunicacion-de-Datos
unidad:
tema:
tags: []
---
## Clase 27/3
- Necesidades de evolucion de una red
- Componentes de una red
- Importancia del Modelo OSI
	- Capa fisica (CAPA 1): define el medio en el que se transmiten los datos (aire cobre, fibraoptica)
	- Capa de Enlace (CAPA 2): La capa de enlace de datos es muy similar a la capa de red, excepto que la capa de enlace de datos facilita la transferencia de datos entre dos dispositivos dentro la _misma_ red.
	- Capa de Red (CAPA 3): La [capa de red](https://www.cloudflare.com/learning/network-layer/what-is-the-network-layer/) es responsable de facilitar la transferencia de datos entre dos redes diferentes. IP
	- Capa de transporte (CAPA 4): La capa 4 es la responsable de las comunicaciones de extremo a extremo entre dos dispositivos. Esto implica, antes de proceder a ejecutar el envío a la capa 3, tomar datos de la capa de sesión y fragmentarlos seguidamente en trozos más pequeños llamados segmentos. TCP
	- Capa de sesion (CAPA 5): La capa de sesión es la responsable de la apertura y cierre de comunicaciones entre dos dispositivos.
	- Capa de presentacion (CAPA 6): Esta capa es principalmente responsable de preparar los datos para que los pueda usar la capa de aplicación; en otras palabras, la capa 6 hace que los datos se preparen para su consumo por las aplicaciones. La capa de presentación es responsable de la traducción, [el cifrado](https://www.cloudflare.com/learning/ssl/what-is-encryption/) y la compresión de los datos.
	- Capa de Aplicacion (CAPA 7): Esta es la única capa que interactúa directamente con los datos del usuario.
