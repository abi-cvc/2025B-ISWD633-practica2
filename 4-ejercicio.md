## Esquema para el ejercicio
![Imagen](esquema-4-ejercicio.PNG)

### Crear la red
# COMPLETAR
docker network create net_practica4 -d bridge

### Crear el contenedor mysql a partir de la imagen mysql:8, configurar las variables de entorno necesarias
# COMPLETAR
docker run -d --name mysql --network net_practica4 -e MYSQL_ROOT_PASSWORD=carol -e MYSQL_DATABASE=wordpress_db -e MYSQL_USER=wordpress_user -e MYSQL_PASSWORD=carol123 mysql:8

### Crear el contenedor wordpress a partir de la imagen: wordpress, configurar las variables de entorno necesarias
# COMPLETAR
docker run -d --name wordpress --network net_practica4 -p 9300:80 -e WORDPRESS_DB_HOST=mysql:3306 -e WORDPRESS_DB_USER=wordpress_user -e WORDPRESS_DB_PASSWORD=carol123 -e WORDPRESS_DB_NAME=wordpress_db wordpress

De acuerdo con el trabajo realizado, en el esquema del ejercicio el puerto a es **(completar con el valor)**

Ingresar desde el navegador al wordpress y finalizar la configuración de instalación.
# COLOCAR UNA CAPTURA DE LA CONFIGURACIÓN

Desde el panel de admin: cambiar el tema y crear una nueva publicación.
Ingresar a: http://localhost:9300/ 
recordar que a es el puerto que usó para el mapeo con wordpress
# COLOCAR UNA CAPTURA DEL SITO EN DONDE SEA VISIBLE LA PUBLICACIÓN.

### Eliminar el contenedor wordpress
# COMPLETAR

### Crear nuevamente el contenedor wordpress
Ingresar a: http://localhost:9300/ 
recordar que a es el puerto que usó para el mapeo con wordpress

### ¿Qué ha sucedido, qué puede observar?
# COMPLETAR

