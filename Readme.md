# Tarea Trabajando con Volumenes

1.  Para **descargar** las **imagenes** se debe de usar el comando `docker pull nombreImagen:suVersion`, en este caso es `docker pull httpd` 

2. Para **crear** un **contenedor** con un **nombre** de **nuestra elección** se debe usar `docker run --name nombreQueElegimos imagen:version`, usando el comando con los valores que se pidio seria `docker run --name dam_httpd httpd`

3. Eliminar la maquina `docker stop nombreContenedor` y luego `docker rm nombreContenedor` y volver a lanzar el contenedor pero esta vez con un puerto establecido, en el que tenemos que dar con el comando ` docker run -it -p 8000:80 -v /home/dam2/Materias/sxe/volumenes/htdocs:/usr/local/apache2/htdocs --name dam_httpd httpd`, donde establecemos el puerto de `host:contenedor`, luego la carpeta que queremos usar que se vincule con el contenedor al usar el `-v`, y luego se le da nombre con `--name`, para luego ingresar la imagen

4. Para hacer eso solo se tiene que repetir el paso anterior.

5. Para poder ver el html en el navegador se debe de tener la carpeta **htdocs**, al mismo nivel que vinculamos carpetas, con un **index.html**, en el que contenga una **etiqueta** que poseea un hola mundo, para ingresar se debe de ingresar la **ip de la maquina**, es decir, **host:puerto**  o un **localhost:puerto**

6. Para hacer esto se debe de usar `docker run -it -p 9080:80 -v /home/dam2/Materias/sxe/volumenes/htdocs:/usr/local/apache2/htdocs --name dam_web httpd`, donde solo se cambio el puerto y el nombre del contenedor