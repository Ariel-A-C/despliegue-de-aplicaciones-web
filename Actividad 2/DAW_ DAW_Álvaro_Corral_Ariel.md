# Administración de servidores web

## 1. Instale en una máquina virtual un sistema operativo con base Linux (se recomienda Debian o Ubuntu) e instale apache2.

![Captura (61)](https://github.com/Ariel-A-C/despliegue-de-aplicaciones-web/assets/144775269/228b9437-50b3-4391-b663-e269803b639c)


## 2. Explique con sus palabras que es una petición GET, POST, PUT y DELETE, remarcando sus diferencias.
•	GET: lee información del servidor.
•	POST: crea nuevos recursos.
•	PUT: actualiza información recursos existentes.
•	DELETE: elimina recursos.


## 3. Cambie del puerto 80 al puerto 4444 el servidor apache2. Muestra desde el navegador su funcionamiento adjuntando una captura de pantalla.

![Captura (62)](https://github.com/Ariel-A-C/despliegue-de-aplicaciones-web/assets/144775269/d0ec4ea7-b3f4-4b92-a803-acb257e0ccdc)

 
## 4. Instale un certificado SSL y configure su Apache para servir contenido a través de HTTPS en el puerto 4444. Muestre desde el navegador cómo se muestra el sitio web como "seguro" (aunque sea un certificado autofirmado).

![Captura (63)](https://github.com/Ariel-A-C/despliegue-de-aplicaciones-web/assets/144775269/7841caeb-e5cf-4133-9e66-00a08783b841)


## 5. ¿Dónde se encuentran los ficheros de configuración de Apache2?
•	Ubicación principal.

![Captura (64)](https://github.com/Ariel-A-C/despliegue-de-aplicaciones-web/assets/144775269/5f87e206-ae52-4101-9c37-e45c8d8ffb6a)

•	Explora el archivo apache2.conf. Identifica las secciones principales y describe su propósito.

Resumen del archivo de configuración.

![Captura (65)](https://github.com/Ariel-A-C/despliegue-de-aplicaciones-web/assets/144775269/a085f39d-0982-4aee-993d-90c9842166b0)

Configuración global.

![Captura (66)](https://github.com/Ariel-A-C/despliegue-de-aplicaciones-web/assets/144775269/d6414fdd-5405-43c2-813c-30108a56259d)

Opciones de seguridad.

![Captura (67)](https://github.com/Ariel-A-C/despliegue-de-aplicaciones-web/assets/144775269/2aa92563-0832-4951-b313-5229e6c01eb1)

Formatos de logs.

![Captura (68)](https://github.com/Ariel-A-C/despliegue-de-aplicaciones-web/assets/144775269/8404e46b-087a-4d34-9c42-40130eac928f)

•	sites-available y sites-enabled: Explica la diferencia entre estos dos directorios y cómo funcionan juntos.
Ficheros de configuración de Virtual Hosts de Apache2 / Enlaces simbólicos a las configuraciones de sites-avaliable. ‘enabled’ tiene como accesos directos a las configuraciones de ‘avaliable’ para poder activarlas o desactivarlas sin tener que reescribirlas.

•	mods-available y mods-enabled: Explica la diferencia entre estos dos directorios.
Lo mismo excepto que con módulos.


## 6. ¿Dónde se encuentran los ficheros de ejecución de Apache2?
•	Ubicación principal

![Captura (90)](https://github.com/Ariel-A-C/despliegue-de-aplicaciones-web/assets/144775269/2b8dae55-43b3-4443-b4e7-d4b885f85a40)

•	Control del servicio: Utiliza el binario de ejecución para iniciar, detener, recargar y reiniciar el servidor Apache2 explicando la diferencia entre cada uno de los comandos utilizados.

![Captura (91)](https://github.com/Ariel-A-C/despliegue-de-aplicaciones-web/assets/144775269/6592f8c6-aaa5-4ab8-a4ef-5d146a44a903)
![Captura (92)](https://github.com/Ariel-A-C/despliegue-de-aplicaciones-web/assets/144775269/4aab9a76-ee0d-4e7e-af0e-afe0256a1b8d)
![Captura (93)](https://github.com/Ariel-A-C/despliegue-de-aplicaciones-web/assets/144775269/78f8d401-a26f-4bc9-812a-af3c82680fbf)

•	Comprobación de sintaxis: Usa el binario de Apache para verificar la sintaxis de tu configuración. Esto es útil para asegurarse de que no haya errores antes de reiniciar el servidor.

![Captura (94)](https://github.com/Ariel-A-C/despliegue-de-aplicaciones-web/assets/144775269/53b63c4f-7cce-4159-a8df-86628bdf269e)


## 7. ¿Dónde se encuentran los ficheros de monitorización de Apache2?
•	Ubicación principal

![Captura (85)](https://github.com/Ariel-A-C/despliegue-de-aplicaciones-web/assets/144775269/ce2913f4-fd13-4f7a-b29d-08026556fdfe)

•	error.log y access.log: Explica la diferencia entre estos dos archivos. Abre y revisa las entradas recientes en cada uno de ellos.
error.log contiene avisos y errores del servidor y access.log contiene información sobre los visitantes del servidor.

![Captura (87)](https://github.com/Ariel-A-C/despliegue-de-aplicaciones-web/assets/144775269/883efffb-b6fd-4325-a80f-b955db0bdaa0)
![Captura (86)](https://github.com/Ariel-A-C/despliegue-de-aplicaciones-web/assets/144775269/004f5819-4dea-4e50-84a9-60a6a72983e8)

•	Rotación de logs: Investiga cómo funciona la rotación de logs en Apache2. ¿Por qué es importante? ¿Cómo se configura?
Para que no se sature con los logs se van archivando y creando unos nuevos.

•	Monitorización en tiempo real: Utiliza herramientas como tail -f para monitorear en tiempo real los accesos a tu servidor web y posibles errores.

![Captura (88)](https://github.com/Ariel-A-C/despliegue-de-aplicaciones-web/assets/144775269/bb7aa811-e6e4-4c2c-828d-7f5c47026a95)

•	Análisis de logs: Instala y usa herramientas como goaccess para analizar y obtener estadísticas visuales a partir de tus logs de Apache2.

![Captura (95)](https://github.com/Ariel-A-C/despliegue-de-aplicaciones-web/assets/144775269/3da8608e-9915-4fe0-8524-47e7d6f8b618)
![Captura (98)](https://github.com/Ariel-A-C/despliegue-de-aplicaciones-web/assets/144775269/da782649-e354-4c8b-85ef-e62b3eafd329)


## 8. ¿Qué es un Firewall? ¿Para qué sirve? ¿Por qué es necesario? Instale y configure un Firewall en la máquina virtual para que solo permita tráfico HTTP y HTTPS. Bloquee todo el resto de los puertos y demuestre su funcionamiento.
Un firewall es un dispositivo de seguridad de la red que monitoriza el tráfico entrante y saliente y decide si debe permitir o bloquear un tráfico específico en función de un conjunto de restricciones de seguridad ya definidas. Es necesario para aumentar la seguridad del ordenador.

![Captura (89)](https://github.com/Ariel-A-C/despliegue-de-aplicaciones-web/assets/144775269/f479316e-02c4-4c80-ac47-e0566917172e)

## 9. Explica con tus palabras las diferentes partes de una URL.
- Protocolo: el sistema de intercambio de información por internet que se está siguiendo.
- Subdominio: la sección del “sitio” que tiene la web.
- Nombre del dominio: el “sitio” que tiene la web (anfitrión).
- Puerto: puerto de red por el cual se conecta el ordenador.
- Ruta: el camino de subdirectorios por el que se llega.
- Separador de consulta: simplemente separa partes de la URL.
- Parámetros: una especie de variables que señalan cosas como el idioma, el número de página, una búsqueda…
- Fragmento: señala en qué parte de la web se está exactamente.

![image](https://miro.medium.com/v2/resize:fit:1400/1*O2QB8zBNMs7SN44AhGdPrg.png)

## 10. Explica el funcionamiento del protocolo HTTP con tus palabras.
En el protocolo HTTP, un cliente (navegador web) envía una petición a un servidor con un mensaje. Después, el servidor devuelve una respuesta al cliente. Las peticiones usan algunos de los comandos disponibles según lo que quieran del servidor. 

## 11. ¿Qué es un archivo .htaccess? Proporcione un ejemplo de cómo se puede utilizar para reescribir URL o restringir el acceso a ciertas partes de su sitio web.
Los ficheros .htaccess son ficheros de configuración distribuida. Facilitan una forma de realizar cambios en la configuración en contexto directorio. Un fichero, que contiene una o más directivas, se coloca en un documento específico de un directorio, y estas directivas aplican a ese directorio y todos sus subdirectorios.
