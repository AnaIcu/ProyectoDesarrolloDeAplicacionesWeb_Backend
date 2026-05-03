# Backend - Aplicación de Tareas y Metas

## Descripción

Este proyecto consiste en el desarrollo de un backend para una aplicación web que permite gestionar tareas y metas personales (To-Do List). La aplicación permite agregar, listar y eliminar tanto tareas como metas, incluyendo una fecha límite para cada elemento.

## Tecnologías utilizadas

* Node.js (se creó con Node JS v24.13.1)
* npm

## Instalación

Dado que la carpeta `node_modules` no está incluida en el repositorio, es necesario instalar las dependencias antes de ejecutar el proyecto.

1. Clonar el repositorio:
git clone <https://github.com/AnaIcu/ProyectoDesarrolloDeAplicacionesWeb_Backend/tree/semana3>

2. Instalar dependencias:

<npm install>

## Ejecución del proyecto

1. Ejecutar el siguiente comando: npm start
2. El servidor se ejecutará en: http://localhost:3000


## Autenticación

El backend utiliza un middleware de autorización. Todas las peticiones deben incluir el siguiente header:

------------------------
Authorization: 123456
------------------------

Si no se incluye este header o es incorrecto, el servidor responderá con un error 401 (Unauthorized).

## Endpoints disponibles

### Tareas

* Obtener todas las tareas
  GET `/tasks/getTasks`

* Agregar una nueva tarea
  POST `/tasks/addTask`

* Eliminar una tarea
  DELETE `/tasks/removeTask/:id`

### Metas

* Obtener todas las metas
  GET `/goals/getGoals`

* Agregar una nueva meta
  POST `/goals/addGoal`

* Eliminar una meta
  DELETE `/goals/removeGoal/:id`

## Estructura de datos

Tanto las tareas como las metas manejan la siguiente estructura:

{
  id_: number (esta se genera automáticamente),
  name: string,
  description: string,
  duedate: string
}