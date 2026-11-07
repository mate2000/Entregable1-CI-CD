# Entregable1-CI-CD
Taller #1 del curso de CI/CD
Integrantes: Mateo Montoya Aristizabal
GitHub User:mate2000

#1 – 

Se configuraron dos eventos que disparan el workflow. El primero es push, que lo ejecuta automáticamente cada vez que alguien hace push a la rama principal. El segundo es workflow_dispatch, que permite ejecutarlo manualmente desde la pestaña Actions de GitHub cuando sea necesario.

#2 – 

El workflow corre en un runner hospedado por GitHub cuyo sistema operativo reporta el kernel Linux 7.0.0-1019-azure, es decir, una imagen de Ubuntu ejecutándose sobre una máquina virtual.

Todos los comandos de shell definidos en el workflow se ejecutan dentro de esa máquina virtual (runner). Por eso, la información que devuelven (sistema operativo, archivos, variables de entorno, red, etc.) corresponde al runner, que está alojado en un centro de datos remoto.

#3 -

En el Marketplace de GitHub podemos encontrar acciones como fastlane (https://github.com/marketplace?query=fastlane), una herramienta que facilita la compilación, firma y publicación de aplicaciones móviles, y Xygeni Security (https://github.com/marketplace/xygeni-security), una plataforma que ayuda a entregar software seguro más rápido al analizar el código, las dependencias y el pipeline en busca de vulnerabilidades.

#4 -
Un secreto en GitHub Actions es un dato sensible, como una API key, un token, una contraseña o un certificado de firma, que el workflow necesita para ejecutarse, por ejemplo para compilar, firmar o desplegar una aplicación. Escribirlo directamente en el archivo .yaml es muy peligroso, porque cualquiera con acceso al repositorio podría verlo y quedaría guardado en el historial de Git. Por eso se almacena cifrado en la configuración del repositorio

#5 -
En mi día a día como desarrollador de software es muy común subir nuevos cambios de código al repositorio. Ahí GitHub Actions resulta muy útil para la integración continua (CI), porque permite validar automáticamente cada cambio: la calidad del código, el formato, las pruebas y los posibles riesgos de seguridad, entre otras cosas. También sirve para la entrega continua (CD), al automatizar todo el proceso de despliegue del software. En mi caso, como desarrollador móvil, esto es especialmente valioso, ya que el despliegue es más complejo al tener que manejar dos plataformas distintas, iOS y Android, cada una con sus propios procesos de compilación, firma y publicación en las tiendas.
