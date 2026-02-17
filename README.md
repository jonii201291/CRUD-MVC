<h1 align="center">CRUD de Alumnos en PHP con MVC</h1>

Este proyecto implementa un sistema completo CRUD (Create, Read, Update, Delete) para gestionar alumnos.

Está desarrollado en PHP utilizando arquitectura MVC.

Incluye autenticación previa mediante login.

<h3>Funcionalidades</h3>

-Listar alumnos registrados

-Crear nuevos alumnos

-Editar información existente

-Eliminar alumnos

-Acceso protegido mediante login

<h3>Estructura MVC</h3>

models/Alumno.php → operaciones con base de datos
models/User.php → operaciones con base de datos

controllers/AlumnoController.php → lógica CRUD
controllers/AuthController.php → lógica CRUD

views/listar.php → listado en tabla

views/crear.php → formulario de creación

views/editar.php → formulario de edición

views/login.php → formulario de autenticación de los usuarios

index.php → enrutador principal

<h3 align="center">Operaciones CRUD</h3>

Listar

Se muestran todos los alumnos en una tabla desde listar.php.

<img width="1400" height="707" alt="image" src="https://github.com/user-attachments/assets/91b5ffc6-b926-4579-aa59-f4b9cab6aecb" />

Crear

Vista: views/crear.php

<img width="780" height="507" alt="image" src="https://github.com/user-attachments/assets/741dee27-d167-4b30-aab9-7519ead1c3bd" />

Editar

Vista: views/editar.php

<img width="780" height="492" alt="image" src="https://github.com/user-attachments/assets/8a81f2b5-1850-4c07-8841-6e6a22ea9693" />

Eliminar

No tiene vista propia, solo redirección.

<img width="822" height="312" alt="image" src="https://github.com/user-attachments/assets/a874caff-e484-4f86-aa86-97e991a60c32" />

Vistas principales

login.php → pantalla de inicio desesión como usuario

<img width="625" height="415" alt="image" src="https://github.com/user-attachments/assets/2bf9386a-aa91-4d52-ba90-0ba8c73f3118" />

listar.php → tabla de contenido con acciones editar/eliminar

<img width="834" height="745" alt="image" src="https://github.com/user-attachments/assets/52a2535c-e158-4dca-a5be-f7f2c40f7179" />

crear.php → formulario de alta

<img width="631" height="655" alt="image" src="https://github.com/user-attachments/assets/0a2fb018-975a-47b4-9e92-62493a3bfdd5" />

editar.php → formulario de modificación

<img width="628" height="657" alt="image" src="https://github.com/user-attachments/assets/08628984-6f68-49d6-89df-fd82f2852d0e" />

Base de datos

Tabla utilizada para los usuarios:
<img width="867" height="221" alt="image" src="https://github.com/user-attachments/assets/55f6a47c-b847-4575-adca-08373332fb20" />

Tabla utilizada para los alumnos:
<img width="961" height="148" alt="image" src="https://github.com/user-attachments/assets/f2676e1d-fd1c-41ff-9426-ddfc45eddef2" />

Ejecución

Activar la funcionalidad de Apache y MySQL en XAMPP

Una vez estén corriendo las dos, desde el navegador:

localhost/nombreProyecto/index.php

Problemas

Desde la URL si se accede a cualquier vista, se abre, esto no debería pasar puesto que para acceder a esas vistas tiene que haber un id de usuario activo. Todas las vistas deberían ir a la vitsta de login.php

Mejoras

En la versión mejorada se deberían poder crear usuarios desde un usuario único de control, con normas específicas en ambos campos como poner un texto alfanumérico de mínimo 3 caracteres como usuario y de mínimo 9 caracteres que contengan mayúsculas, minúsculas, números y caracteres especiales en la contraseña.
