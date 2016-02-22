##Notacion de parametros necesaria para cada comando
Ademas de las opciones especificas de cada comando, la aplicacion necesitara de parametros de autentificacion Oauth de la API de Github, que seran cargados cada vez que se realice cualquier accion.

Estos parametros son:

--username

El nombre de usuario de github, si no se indica por defecto se cargara el nombre del usuario del sistema.

--password

La contraseña del usuario de Github, es un parametro requerido.

--token

El token con los permisos especificos creados para la aplicacion explicado en la [guia de instalacion](/instalacion.md).

--api

--web

###Usando variables de entorno ENV
Una buena manera de ahorrarnos tiempo y hacer menos incomodo la insercion de estos parametros cada vez que tenegamos que ejecutar una accion, es hacer uso de las variables de entorno. Guardar el token en una variable, el usuario de github y la contraseña, haran mas agil el manejo de comandos.

Una manera sencilla de añadir una variable de entorno es abrir una terminal y ejecutar:
```bash
vi /home/tupropiousuario/.bashrc
```
Modificando /tupropiousuario/ por tu usuario de sistema, con este comando se abrira el archivo donde se cargan las variables de entorno en el sistema (en vez de vi puedes usar el editor que mas te guste). Alli podremos asignar las variables que nos interesen.

Por ejemplo:
TEACHERS_PET_TOKEN=4e409b9c61bf9652c32023d83af9d61af47f

Despues de guardar el archivo hace falta volver a cargarlo para que los cambios sean efectivos.

```bash
source /home/tupropiousuario/.bashrc
```
Si quieres comprobar que la variable se ha guardado y cargado correctamente se puede mirar facilmente de esta forma.

```bash
echo $TEACHERS_PET_TOKEN
```

Para poder invocar a una variable de entorno hace falta usar el simbolo $, por lo que este caso en el parametro habria seria llamado tal que ``--token=$TEACHERS_PET_TOKEN ``


##Crear equipos de estudiantes

teachers_pet create_student_teams

Es necesario tener un archivo sin formato "students", donde los grupos esten asignados en cada linea. Por defecto se supondra el directorio raiz como la ruta asignada al archivo, pero esto podra ser modificado mediante el parametro --students donde se la podra asignar la nueva ruta al archivo y su formato. 

Si queremos un grupo individual en la linea debe estar solamente el nombre de un alumno.

Ejemplo:

studentBeta

Si queremos un grupo en primer lugar se debera escribir el nombre del grupo, y despues asignar los usuarios.

TeamA studentBeta studentAlpha1


##Añadir a un equipo

add_to_team

Es necesario crear un archivo, el nombre del archivo sera el equipo, y los usuarios estaran contenidos en el.

##Ver quien ha hecho un fork de un repositorio
