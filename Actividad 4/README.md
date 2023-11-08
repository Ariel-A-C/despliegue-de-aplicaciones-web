# P4: Servidores virtuales de Apache

Crea dos sitios web que compartirán IP y puerto, pero tendrán nombres DNS distintos
para acceder a ellos. El nombre del primer dominio será daw.gimbernat.eug.es y el
segundo tunombreyapellidos.gimbernat.eug.es, donde “tunombreyapellidos” contiene
la inicial de tu nombre, el primer apellido, y la inicial de tu segundo apellido. De esta
manera, si tu nombre es: Francisco Mesas Cervilla, el domino quedaría:
fmesasc.gimbernat.eug.es.

- En el primer caso, daw.gimbernat.eug.es tendrá su directorio base en
/var/www/daw/ conteniendo una página llamada index.html que ponga el
nombre de la clase como título con un archivo css para aplicarle estilos al título.
- En el segundo caso, fmesasc.gimbernat.eug.es tendrá su directorio base en
/var/www/fmesasc/ (el equivalente para vuestros nombres), conteniendo una
página llamada index.html que contenga vuestro currículum aplicándole un
estilo css para que se visualice correctamente.

Para ello, tendrás que crear un archivo de configuración (copiado de 000-default.conf)
para cada uno de los dominios. Recuerda que con a2ensite puedes crear los enlaces
simbólicos necesarios para añadir esta configuración a la ejecución de apache

![Captura (133)](https://github.com/Ariel-A-C/despliegue-de-aplicaciones-web/assets/144775269/c6eab3af-3b4e-4c8d-aeb8-184dabd4d46a)
![Captura (136)](https://github.com/Ariel-A-C/despliegue-de-aplicaciones-web/assets/144775269/6bc0c18e-7deb-4c51-93b7-c6f79fda3c99)
![Captura (135)](https://github.com/Ariel-A-C/despliegue-de-aplicaciones-web/assets/144775269/eb32bcb3-1a7a-49a1-9369-ab956f72abe9)
![Captura (134)](https://github.com/Ariel-A-C/despliegue-de-aplicaciones-web/assets/144775269/b306db53-3c68-49e0-9771-9cf7ff13f294)

![Captura (137)](https://github.com/Ariel-A-C/despliegue-de-aplicaciones-web/assets/144775269/f308737d-0f8b-42c2-93bd-d711b81f7205)
![Captura (138)](https://github.com/Ariel-A-C/despliegue-de-aplicaciones-web/assets/144775269/27bc32de-b3ed-4510-92d0-3ee8f3f469ee)
