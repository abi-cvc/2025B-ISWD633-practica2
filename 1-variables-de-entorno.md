# Variables de Entorno
### ¿Qué son las variables de entorno?
# COMPLETAR
Las variables de entorno son variables dinámicas, que tienen un nombre que les identifica y un valor. Se utilizan para la configuración de aplicaciones, sistema operativo, etc. 
Almacenan información como rutas de directorios, configuración de aplicaciones o credenciales de bases de datos, permitiendo que la misma aplicación se ejecute de forma diferente según el entorno (desarrollo, pruebas, producción) sin necesidad de modificar su código

### Para crear un contenedor con variables de entorno

```
docker run -d --name <nombre contenedor> -e <nombre variable1>=<valor1> -e <nombre variable2>=<valor2>
```

### Crear un contenedor a partir de la imagen de nginx:alpine con las siguientes variables de entorno: username y role. Para la variable de entorno rol asignar el valor admin.

# COMPLETAR

# CAPTURA CON LA COMPROBACIÓN DE LA CREACIÓN DE LAS VARIABLES DE ENTORNO DEL CONTENEDOR ANTERIOR
<img width="1306" height="137" alt="image" src="https://github.com/user-attachments/assets/2f55dde8-f736-4cc5-93ad-ef68fba8e2bf" />
Con docker inspect practica2
<img width="1513" height="1290" alt="image" src="https://github.com/user-attachments/assets/480e72ce-a26c-42f2-9cf5-6c944a0f4060" />



### Crear un contenedor con la imagen de mysql, mapear todos los puertos
# COMPLETAR
docker pull mysql
docker images
docker run -d --name new_container mysql:latest

### ¿El contenedor se está ejecutando?
# COMPLETAR
no se está ejecutando
<img width="2519" height="597" alt="image" src="https://github.com/user-attachments/assets/750b46e7-428b-426f-ba9f-d57d8d065b75" />


### Identificar el problema
# COMPLETAR

### Para crear un contenedor con variables de entorno especificadas
- Portabilidad: Las aplicaciones se vuelven más portátiles y pueden ser desplegadas en diferentes entornos (desarrollo, pruebas, producción) simplemente cambiando el archivo de variables de entorno.
- Centralización: Todas las configuraciones importantes se centralizan en un solo lugar, lo que facilita la gestión y auditoría de las configuraciones.
- Consistencia: Asegura que todos los miembros del equipo de desarrollo o los entornos de despliegue utilicen las mismas configuraciones.
- Evitar Exposición en el Código: Mantener variables sensibles como contraseñas, claves API, y tokens fuera del código fuente reduce el riesgo de exposición accidental a través del control de versiones.
- Control de Acceso: Los archivos de variables de entorno pueden ser gestionados con permisos específicos, limitando quién puede ver o modificar la configuración sensible.

### Crear un contenedor con mysql, mapear todos los puertos y configurar las variables de entorno mediante un archivo
# COMPLETAR

# CAPTURA CON LA COMPROBACIÓN DE LA CREACIÓN DE LAS VARIABLES DE ENTORNO DEL CONTENEDOR ANTERIOR 

### ¿Qué bases de datos existen en el contenedor creado?
docker run -d --name new_container -e MYSQL_ROOT_PASSWORD=admin123 -p 3306:3306 mysql:latest
docker exec -it new_container mysql -u root -p

mysql> SHOW DATABASES;

# COMPLETAR
Las bases de datos que existen en el contenedor son:
- information_schema
- mysql
- performance_schema
- sys

<img width="2500" height="952" alt="image" src="https://github.com/user-attachments/assets/382e934d-2f19-46f5-95f0-2bf6fabdabe9" />
