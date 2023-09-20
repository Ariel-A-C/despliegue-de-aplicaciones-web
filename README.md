# despliegue-de-aplicaciones-web

### Analiza los headers de las peticiones cuando inicias sesión en el Moodle y comprende cómo se obtiene el token. Para ello, necesitamos saber de dónde salen TODOS los datos sensibles que se envían.
![3.1](https://github.com/Ariel-A-C/despliegue-de-aplicaciones-web/assets/144775269/c419dc78-fa89-4db5-8fcb-2b1a9d071884)
![3.2](https://github.com/Ariel-A-C/despliegue-de-aplicaciones-web/assets/144775269/bc497418-cbc7-4d2d-9caf-096d74953afc)

### ¿A qué puerto se reciben normalmente las peticiones del protocolo HTTP? ¿A qué capa del modelo TCP/IP se encuentra el protocolo HTTP? ¿Y los protocolos TCP, UDP, e IP?
En TCP el puerto por defecto, para un servidor HTTP en un computador, es el puerto 80. El protocolo HTTP se encuentra en la capa de aplicación del model TCP/IP. Los protocolos TCP, UDP e IP se encuentran en las capas de transporte, transporte e internet respectivamente.

### ¿Cuál es el significado de la siguiente respuesta de un servidor?
`HTTP/1.1 302 Found   
Location: http://www.example.com/test/index2.php`
El código de estado de redirección HTTP 302 Found indica que el recurso solicitado ha sido movido temporalmente a la URL dada por las cabeceras Location. Un navegador redirecciona a esta página, pero los motores de búsqueda no actualizan sus enlaces al recurso.

### Utilizando el filtro de captura para la interfaz de red de Wireshark, analiza la petición al host: www.google.com. Mostrando la cabecera IP, la dirección IP de tu ordenador y la del servidor. Comprueba que, poniendo esa IP en el navegador, accedas a Google.
