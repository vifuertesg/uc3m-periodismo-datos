## METODOLOGÍA
A continuación, voy explicar brevemente qué pasos he seguido para agrupar todos mis trabajos en esta página web:

El primer paso ha sido organizar todos los contenidos que aquí presento en sus carpetas correspondientes, de esta manera me va a ser más sencillo acceder a ellos. También he tenido que cambiar la ruta de algunas imágenes para que fuera posible su visualización en esta página web. 

Posteriormente, me he descargado Pandoc desde [Pandoc.org](https://pandoc.org/installing.html) para poder convertir todos estos archivos a formato HTML. Esta conversión la he realizado a través de la terminal siguiendo el siguiente modelo:  pandoc ruta/archivo.md -o ruta/archivo.index.html. Una vez los he transformado, he creado una carpeta llamada doc para recopilar todas estas prácticas en el formato HTML.

Con los comandos git add, git commit y git push he subido esta carpeta con los archivos transformados a github y las imágenes. A este paso, le ha sigo la descarga de la carpeta "bootstrap-5.1.3-examples.zip", carpeta que he descoprimido con el comando unzip -| en la terminal. De esta nueva carpeta he seleccionado tres archivos (sticky-footer-navbar, css y js), que a través del comando mv he introducido en mi carpeta docs.

Una vez tenia todos los archivos necesarios he procedido a realizar cambios la plantilla: index.html para poder configurar mi página web. De esta manera he realizado acciones tales como introducir los archivos HTML de las prácticas en el apartado "begin page content". Una vez que tenía configurada mi página web he subido la carpeta docs a github y a través de "settings" y la opción "pages" he generado el siguiente link:      que es mi página web.
