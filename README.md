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

controllers/AlumnoController.php → lógica CRUD

views/listar.php → listado en tabla

views/crear.php → formulario de creación

views/editar.php → formulario de edición

index.php → enrutador principal

<h3 align="center">Operaciones CRUD</h3>

Read (Listar)

Se muestran todos los alumnos en una tabla desde listar.php.

$stmt = $this->alumno->read();
$alumnos = $stmt->fetchAll(PDO::FETCH_ASSOC);


Create (Crear alumno)

Vista: views/crear.php

if ($this->alumno->create()) {
    header("Location: index.php?action=index&message=created");
}


Update (Editar alumno)

Vista: views/editar.php

$this->alumno->numAlumno = $_POST['numAlumno'];
$this->alumno->update();


Delete (Eliminar alumno)

No tiene vista propia, solo redirección.

if ($this->alumno->delete()) {
    header("Location: index.php?action=index&message=deleted");
}


Vistas principales

listar.php → tabla con acciones editar/eliminar

crear.php → formulario de alta

editar.php → formulario de modificación

Base de datos

Tabla utilizada:

<img width="1403" height="622" alt="image" src="https://github.com/user-attachments/assets/a8fe7dfb-4942-4834-acf7-15f43f64cd86" />

Ejecución

Iniciar el proyecto desde index.php

Primero se muestra el login

Después se accede al listado CRUD

http://localhost/crud-alumnos-mvc/
