# Administración de servidores web

## 1. Instale en una máquina virtual un sistema operativo con base Linux (se recomienda Debian o Ubuntu) e instale apache2.

![image](https://github.com/Ariel-A-C/despliegue-de-aplicaciones-web/assets/144775269/d48daf77-c1a9-467f-821a-4f3623e57160)


## 2. Explique con sus palabras que es una petición GET, POST, PUT y DELETE, remarcando sus diferencias.
•	GET: lee información del servidor.
•	POST: crea nuevos recursos.
•	PUT: actualiza información recursos existentes.
•	DELETE: elimina recursos.


## 3. Cambie del puerto 80 al puerto 4444 el servidor apache2. Muestra desde el navegador su funcionamiento adjuntando una captura de pantalla.

![image](https://github.com/Ariel-A-C/despliegue-de-aplicaciones-web/assets/144775269/6394e47b-fc48-4d84-bbf1-c8b69deea82a)

 
## 4. Instale un certificado SSL y configure su Apache para servir contenido a través de HTTPS en el puerto 4444. Muestre desde el navegador cómo se muestra el sitio web como "seguro" (aunque sea un certificado autofirmado).

![image](https://github.com/Ariel-A-C/despliegue-de-aplicaciones-web/assets/144775269/9c70fd3a-fb63-4edc-bd82-00030b5892c1)


## 5. ¿Dónde se encuentran los ficheros de configuración de Apache2?
•	Ubicación principal.

![image](https://github.com/Ariel-A-C/despliegue-de-aplicaciones-web/assets/144775269/a03886a4-1f78-4c60-8b66-6703b1d6fc20)

•	Explora el archivo apache2.conf. Identifica las secciones principales y describe su propósito.

Resumen del archivo de configuración.

![image](https://github.com/Ariel-A-C/despliegue-de-aplicaciones-web/assets/144775269/fa8f17de-dd23-460c-972b-a042edc544dd)

Configuración global.

![image](https://github.com/Ariel-A-C/despliegue-de-aplicaciones-web/assets/144775269/6c25f24d-6f8f-4ef5-9654-839e3a6b4c4c)

Opciones de seguridad.

![image](https://github.com/Ariel-A-C/despliegue-de-aplicaciones-web/assets/144775269/81883f1e-26b7-437d-bf02-5537fb659c62)

Formatos de logs.

![image](https://github.com/Ariel-A-C/despliegue-de-aplicaciones-web/assets/144775269/8282b6d9-ad2b-470c-96a8-cd7ce90f4222)

•	sites-available y sites-enabled: Explica la diferencia entre estos dos directorios y cómo funcionan juntos.
Ficheros de configuración de Virtual Hosts de Apache2 / Enlaces simbólicos a las configuraciones de sites-avaliable. ‘enabled’ tiene como accesos directos a las configuraciones de ‘avaliable’ para poder activarlas o desactivarlas sin tener que reescribirlas.

•	mods-available y mods-enabled: Explica la diferencia entre estos dos directorios.
Lo mismo excepto que con módulos.


## 6. ¿Dónde se encuentran los ficheros de ejecución de Apache2?
•	Ubicación principal

![image](https://github.com/Ariel-A-C/despliegue-de-aplicaciones-web/assets/144775269/de2d7dda-f490-4c34-a5fb-e1015f4e69c9)

•	Control del servicio: Utiliza el binario de ejecución para iniciar, detener, recargar y reiniciar el servidor Apache2 explicando la diferencia entre cada uno de los comandos utilizados.

![image](https://github.com/Ariel-A-C/despliegue-de-aplicaciones-web/assets/144775269/d087d066-c6c9-4785-9b53-8ea555797c6d)
![image](https://github.com/Ariel-A-C/despliegue-de-aplicaciones-web/assets/144775269/495ce20e-83f7-4194-afcb-f6633fe356c2)
![image](https://github.com/Ariel-A-C/despliegue-de-aplicaciones-web/assets/144775269/51da7af4-2a96-49f2-b4bb-0d139b8a0409)

•	Comprobación de sintaxis: Usa el binario de Apache para verificar la sintaxis de tu configuración. Esto es útil para asegurarse de que no haya errores antes de reiniciar el servidor.

![image](https://github.com/Ariel-A-C/despliegue-de-aplicaciones-web/assets/144775269/c6b1cf0d-358e-47bf-808c-0ee86505dc3a)


## 7. ¿Dónde se encuentran los ficheros de monitorización de Apache2?
•	Ubicación principal

![image](https://github.com/Ariel-A-C/despliegue-de-aplicaciones-web/assets/144775269/e58516f9-9ac8-4240-9dbe-07dc09b90081)

•	error.log y access.log: Explica la diferencia entre estos dos archivos. Abre y revisa las entradas recientes en cada uno de ellos.
error.log contiene avisos y errores del servidor y access.log contiene información sobre los visitantes del servidor.

![image](https://github.com/Ariel-A-C/despliegue-de-aplicaciones-web/assets/144775269/ea8d1c02-80e5-4337-8991-39f1ef252aba)
 
•	Rotación de logs: Investiga cómo funciona la rotación de logs en Apache2. ¿Por qué es importante? ¿Cómo se configura?
Para que no se sature con los logs se van archivando y creando unos nuevos.

•	Monitorización en tiempo real: Utiliza herramientas como tail -f para monitorear en tiempo real los accesos a tu servidor web y posibles errores.

![image](https://github.com/Ariel-A-C/despliegue-de-aplicaciones-web/assets/144775269/a3526355-b9a3-49f2-ab3b-f8c8f8cdd747)

•	Análisis de logs: Instala y usa herramientas como goaccess para analizar y obtener estadísticas visuales a partir de tus logs de Apache2.

![image](https://github.com/Ariel-A-C/despliegue-de-aplicaciones-web/assets/144775269/f884383c-f342-404f-8bb3-2d55ec0f880d)
![image](https://github.com/Ariel-A-C/despliegue-de-aplicaciones-web/assets/144775269/c98bede5-d548-4ab2-9516-4edeac35c1f9)


## 8. ¿Qué es un Firewall? ¿Para qué sirve? ¿Por qué es necesario? Instale y configure un Firewall en la máquina virtual para que solo permita tráfico HTTP y HTTPS. Bloquee todo el resto de los puertos y demuestre su funcionamiento.
Un firewall es un dispositivo de seguridad de la red que monitoriza el tráfico entrante y saliente y decide si debe permitir o bloquear un tráfico específico en función de un conjunto de restricciones de seguridad ya definidas. Es necesario para aumentar la seguridad del ordenador.

![image](https://github.com/Ariel-A-C/despliegue-de-aplicaciones-web/assets/144775269/a863ecf9-b549-4cb6-a906-e450b005c935)

## 9. Explica con tus palabras las diferentes partes de una URL.
- Protocolo: el sistema de intercambio de información por internet que se está siguiendo.
- Subdominio: la sección del “sitio” que tiene la web.
- Nombre del dominio: el “sitio” que tiene la web (anfitrión).
- Puerto: puerto de red por el cual se conecta el ordenador.
- Ruta: el camino de subdirectorios por el que se llega.
- Separador de consulta: simplemente separa partes de la URL.
- Parámetros: una especie de variables que señalan cosas como el idioma, el número de página, una búsqueda…
- Fragmento: señala en qué parte de la web se está exactamente.

![image](https://github.com/Ariel-A-C/despliegue-de-aplicaciones-web/assets/144775269/0a9991d1-9b5c-4408-b437-173df871475d)

## 10. Explica el funcionamiento del protocolo HTTP con tus palabras.
En el protocolo HTTP, un cliente (navegador web) envía una petición a un servidor con un mensaje. Después, el servidor devuelve una respuesta al cliente. Las peticiones usan algunos de los comandos disponibles según lo que quieran del servidor. 

## 11. ¿Qué es un archivo .htaccess? Proporcione un ejemplo de cómo se puede utilizar para reescribir URL o restringir el acceso a ciertas partes de su sitio web.
Los ficheros .htaccess son ficheros de configuración distribuida. Facilitan una forma de realizar cambios en la configuración en contexto directorio. Un fichero, que contiene una o más directivas, se coloca en un documento específico de un directorio, y estas directivas aplican a ese directorio y todos sus subdirectorios.
