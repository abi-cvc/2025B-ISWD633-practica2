### Crear contenedor de Postgres sin que exponga los puertos. Usar la imagen: postgres:15-alpine3.21
# COMPLETAR
docker create --name Postgres_container postgres:15-alpine3.21
<img width="1237" height="433" alt="image" src="https://github.com/user-attachments/assets/d39d9213-6d6a-4b27-ba0a-43343ca9471e" />


### Crear un cliente de postgres. Usar la imagen: dpage/pgadmin4


# COMPLETAR

La figura presenta el esquema creado en donde los puertos son:
- a: 8080
- b: 80
- c: 5432

![Imagen](esquema-2-ejercicio.PNG)

## Desde el cliente
### Acceder desde el cliente al servidor postgres creado.
# COMPLETAR CON UNA CAPTURA DEL LOGIN
<img width="3830" height="1091" alt="image" src="https://github.com/user-attachments/assets/52d18f88-be54-4d1e-b33f-25b037a19881" />

### Crear la base de datos info, y dentro de esa base la tabla personas, con id (serial) y nombre (varchar), agregar un par de registros en la tabla, obligatorio incluir su nombre.
<img width="3840" height="813" alt="image" src="https://github.com/user-attachments/assets/8847ab2c-fb52-4a3a-9dcf-19a731bb209a" />


## Desde el servidor postgresl
### Acceder al servidor
### Conectarse a la base de datos info
# COMPLETAR
### Realizar un select *from personas
# AGREGAR UNA CAPTURA DE PANTALLA DEL RESULTADO
<img width="786" height="498" alt="image" src="https://github.com/user-attachments/assets/220b05d9-28d2-4950-a4a5-f00220dfa792" />
<img width="671" height="212" alt="image" src="https://github.com/user-attachments/assets/b689c905-8275-4fa0-81ec-4a06e3fdc404" />

