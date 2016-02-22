###Notacion de parametros necesaria para cada comando
Ademas de las opciones especificas de cada comando, la aplicacion necesitara de parametros de autentificacion Oauth de la API de Github, que seran cargados cada vez que se realice cualquier accion.

Estos parametros son:

--username

El nombre de usuario de github, si no se indica por defecto se cargara el nombre del usuario del sistema.

--password

La contraseña del usuario de Github, es un parametro requerido.

--token

El token con los permisos especificos creados para la aplicacion explicado en la ![guia de instalacion](/instalacion.md)

--api

--web

###Crear grupos de estudiantes

teachers_pet create_student_teams

Es necesario tener un archivo sin formato "students", donde los grupos esten asignados en cada linea. Por defecto se supondra el directorio raiz como la ruta asignada al archivo, pero esto podra ser modificado mediante el parametro --students donde se la podra asignar la nueva ruta al archivo y su formato. 

Si queremos un grupo individual en la linea debe estar solamente el nombre de un alumno.

Ejemplo:

studentBeta

Si queremos un grupo en primer lugar se debera escribir el nombre del grupo, y despues asignar los usuarios.

TeamA studentBeta studentAlpha1