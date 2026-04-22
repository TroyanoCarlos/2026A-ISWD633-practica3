# COMPLETAR  
Comparando sus conocimientos antes de hacer la práctica con sus conocimientos después de hacer la tarea, explicar los principales aprendizajes logrados para beneficio de su formación profesional.  
Si solucionó un problema presentado o utilizó otros comandos que no se mencionan al realizar la práctica también se debe documentar.


Aprendí principalmente el uso y comportamiento de volumenes y bind mount. Ahora se crear bind mount y que es necesario crear una ruta en el equipo host e identificar segun la documentacion la ruta en donde se debe asociar ese volumen en el contenedor. Estos bind mount se comportar segun lo que preexista o se copie en la ruta del host. Si por alguna razon esta carpeta del host se corrompe, no funcionara el contenedor y debera vaciarse la carpeta del host.

Algo similar sucede con los volumes, solo que estos se alojan en WSL en la carpeta de Docker, y no es tan accesibles desde el explorador de archivos. Para la version ultima de docker, ahora los volumenes se alojan en \\wsl.localhost\docker-desktop\mnt\docker-desktop-disk\data\docker\volumes y no en la ruta indicada en la guia.

Cabe destacar que la ruta dentro del contenedor para asociar volumes para postgres /var/lib/postgresql/data solo funciona para postgres:17 o menor. Ademas Drupal solo funciona con postgres de 16 o versiones en adelante, entonces para seguir la guia con las explicaciones mostradas, debe usarse postgres:16 o postgres:17
