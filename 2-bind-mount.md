# BIND MOUNT
En un bind mount mapeamos (montar) un directorio o archivo específico del sistema de archivos del host con una parte del sistema de ficheros del contenedor.

```
docker run -d --name <nombre contenedor> -v <ruta carpeta host>:<ruta carpeta contenedor> <imagen> 
```
ó
```
docker run -d --name <nombre contenedor> --mount type=bind,source=<ruta carpeta host>,target=<ruta carpeta contenedor> <imagen>
```
- destination, dst, target: La ruta donde se monta el archivo o directorio en el contenedor.
- source, src: El origen del montaje.
  
### En tu computador crear una carpeta llamada nginx y dentro de esta carpeta crea otra llamada html. Como se aprecia en la figura.
![Volúmenes](directorio.PNG)

### Crear un contenedor con la imagen nginx:alpine, mapear todos por puertos, para la ruta carpeta host colocar el directorio en donde se encuentra la carpeta html en tu computador y para la ruta carpeta contenedor: /usr/share/nginx/html (esta ruta se obtiene al revisar la documentación de la imagen)
![Volúmenes](volumen-host.PNG)
# COMPLETAR CON EL COMANDO

### ¿Qué sucede al ingresar al servidor de nginx?
# COMPLETAR CON LA RESPUESTA A LA PREGUNTA

<img width="1895" height="931" alt="image" src="https://github.com/user-attachments/assets/bd847ce8-feda-4cb3-94ff-49f6ae960f35" />
Al tratar de acceder desde el navegador no se encuentra la página web. Aparece el error 403 Forbidden.
### ¿Qué pasa con el archivo index.html del contenedor?
# COMPLETAR CON LA RESPUESTA A LA PREGUNTA

<img width="1754" height="396" alt="image" src="https://github.com/user-attachments/assets/459655c1-eadd-458b-8934-91f46171de8e" />

Ahora ya no aparece el documento index.html en el contenedor.

### Ir a https://html5up.net/ y descargar un template gratuito, descomprirlo dentro de tu computador en la carpeta html
### ¿Qué sucede al ingresar al servidor de nginx?
# COMPLETAR CON LA RESPUESTA A LA PREGUNTA
<img width="1908" height="967" alt="image" src="https://github.com/user-attachments/assets/f5ee3696-a44e-44d8-afb4-8b2185e420d2" />

Ahora al acceder desde el navegador aparece el template de pagina descargada y descomprimida en la ruta del bind mount.

### Eliminar el contenedor
# COMPLETAR CON EL COMANDO

<img width="531" height="78" alt="image" src="https://github.com/user-attachments/assets/ce916621-678a-48ca-84dd-d52493d10f95" />

### ¿Qué sucede al crear nuevamente un contenedor montado al directorio definidos anteriormente?
# COMPLETAR CON LA RESPUESTA A LA PREGUNTA
Al volver a crear el contenedor y acceder desde el navegador, se puede observar que el template de la pagina web sigue persistiendo por lo que la seguimos viendo sin tener que volver a hacer el proceso de descargar y descomprimir. Esto nos indica que la información del bind mount persiste en nuestro computador en la ruta definida, y no depende de la vida del contenedor.

