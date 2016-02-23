##Crea tu organizacion en Github
Teachers_pet es una libreria para la creacion y control de repositiorios de la plataforma Github. Asi pues, tanto el profesor como los alumnos intereseados en el uso de la aplicacion deben estar registrados como usuarios en [Github](https://github.com/).

Si no se esta familiarizado con el uso de repositorios y de la plataforma Github, existe documentacion para la ayuda al usuario en la propia [web](https://help.github.com/).

###Creacion y uso de la Organizacion.
Para el uso de correcto de la aplicacion es necesario manejar la opcion de Organizaciones de la github, ya que es necesario la creacion previa de una organizacion donde asignar a los alumnos de cada clase. [Tutorial para el uso y manejo de Organizations](https://github.com/blog/674-introducing-organizations).

Tras la creacion de la organizacion, invite a los alumnos a la misma. Tendran que verificar su ingreso para que salgan activos en la clase. La invitacion sera enviada por email.

Tras este ultimo paso estaremos listos para empezar a usar teacher_pet.

##Notacion de parametros necesaria para cada comando
Ademas de las opciones especificas de cada comando, la aplicacion necesitara de parametros de autentificacion Oauth de la API de Github, que seran cargados cada vez que se realice cualquier accion.

Estos parametros son:

`--username`

El nombre de usuario de github, si no se indica por defecto se cargara el nombre del usuario del sistema.

`--password`

La contraseña del usuario de Github, es un parametro requerido.

`--token`

El token con los permisos especificos creados para la aplicacion explicado en la [guia de instalacion](/instalacion.md).

`--api`

`--web`

###Usando variables de entorno ENV
Una buena manera de ahorrarnos tiempo y hacer menos incomodo la insercion de estos parametros cada vez que tenegamos que ejecutar una accion, es hacer uso de las variables de entorno. Guardar el token en una variable, el usuario de github y la contraseña, haran mas agil el manejo de comandos.

Una manera sencilla de añadir una variable de entorno es abrir una terminal y ejecutar:
```bash
$> vi /home/tupropiousuario/.bashrc
```
Modificando /tupropiousuario/ por tu usuario de sistema, con este comando se abrira el archivo donde se cargan las variables de entorno en el sistema (en vez de vi puedes usar el editor que mas te guste). Alli podremos asignar las variables que nos interesen.

Por ejemplo:
`TEACHERS_PET_TOKEN=4e409b9c61bf9652c32023d83af9d61af47f`

Despues de guardar el archivo hace falta volver a cargarlo para que los cambios sean efectivos.

```bash
$> source /home/tupropiousuario/.bashrc
```
Si quieres comprobar que la variable se ha guardado y cargado correctamente se puede mirar facilmente de esta forma.

```bash
echo $TEACHERS_PET_TOKEN
```

Para poder invocar a una variable de entorno hace falta usar el simbolo $, por lo que este caso en el parametro habria seria llamado tal que ``--token=$TEACHERS_PET_TOKEN ``



##Crear equipos de estudiantes

`teachers_pet create_student_teams`

Es necesario tener un archivo sin formato "students", donde los grupos esten asignados en cada linea. Por defecto se supondra el directorio raiz como la ruta asignada al archivo, pero esto podra ser modificado mediante el parametro ```--students``` donde se la podra asignar la nueva ruta al archivo y su formato. 

Si queremos un grupo individual en la linea debe estar solamente el nombre de un alumno.

Ejemplo:

>studentBeta

Si queremos un grupo en primer lugar se debera escribir el nombre del grupo, y despues asignar los usuarios.

>TeamC studentBeta studentAlpha1

Despues ejecutaremos el comando, sustituyendo las variables de entorno del ejemplo por las tuyas, o por los datos directamente.

```bash 
$> teachers_pet create_student_teams --organization=classroom-testing --username=$GITHUB_USER --password=$GITHUB_PASS --token=$TEACHERS_PET_TOKEN
```

Se crearan los equipos de trabajo, y posteriormente se añadaran los usuarios a cada grupo al que han sido asignados.

![](http://i125.photobucket.com/albums/p79/NooK1e_RG/gitbook/teamc_zpsuy5mfxuh.png)

Si vamos a nuestra organizacion en Github podremos ver que efectivamente se ha creado el equipo y se a asignado a los integrantes en el.

![](http://i125.photobucket.com/albums/p79/NooK1e_RG/gitbook/teamCyes_zpsqnibbodi.png)

##Añadir personas a un equipo

`teachers_pet add_to_team`

Es necesario crear un archivo, el titulo o nombre del archivo sera el equipo a manejar, y los usuarios a añadir estaran contenidos en el.

La ruta del archivo sera indicada con el parametro ```--members```.

Para nuestro ejemplo hemos creado un archivo llamado *TeamH* en el que hemos asignado escrito dentro de el al estudiante *studentbeta* 

```bash 
$> teachers_pet add_to_team --organization=classroom-testing --members=./TeamH
```
Aunque no aparezca en el ejemplo, recuerda siempre añadir al comando los parametros de autentificacion.

![](http://i125.photobucket.com/albums/p79/NooK1e_RG/gitbook/addto_zpsg0smy3ee.png)

Vemos como el estudiante ha sido asignado al equipo.



##Creando repositorios para una tarea o asignacion
`teachers_pet create_repos`

Con este comando podremos asignar un asignacion de un repositorio a uno o varios estudiantes. Para ello debemos tener un fichero por defecto *./students* o añadir la ruta con el parametro ```--students```.
Antes de poder trabajar con issues, clonar, y las demas opciones, es necesario seguir este paso primero.

Vamos a crear un repositorio para los alumnos* studentalpha1* y *studentbeta*, el repositorio se llamara *easytask* y debera ser asignado a ambos alumnos que previamente han sido añadidos a equipos en este caso individuales.

```bash 
teachers_pet create_repos --organization=classroom-testing --repository=easytask --public=true
```

![](http://i125.photobucket.com/albums/p79/NooK1e_RG/gitbook/easy-task_zpsjfdyfi3m.png)


El parametro ```--repository``` asigna el nombre al repositorio.

Con `--public=true` indicamos que es un repositorio publico, si no se posee una cuenta premium de github la operacion no estaria permitida a menos que no se indique que no es un repositorio privado.

![](http://i125.photobucket.com/albums/p79/NooK1e_RG/gitbook/easytask-done_zps3i7uhwlq.png)

Podemos ver que se ha creado la asignacion de los estudiantes a los repositorios.

##Rellenado el repositorio y ejecutando Push Files
`teachers_pet push_files`

Tras haber creado el repositorio vacio y haber sido asignado con **create_repos**, podremos rellenarlo con un plantilla base para nuestros alumnos empiecen a trabajar en el repository. Por ejemplo que el repositorio tenga *gitignore, rakefile, makefile,* etc. Tras haberlo creado desde nuestro repositorio local usaremos el comando **push_files** para añadir ese codigo a todos los alumnos a los que se les ha asginado la tarea del repositorio. Este comando funciona creando un Git Remote por cada repositorio del estudiante y haciendo despues un Git Push a cada uno de ellos.

```bash
teachers_pet push_files --organization=classroom-testing --repository=easytask
```
En este caso ejecutando el comando, enviariamos el contenido del repositorio a las asignaciones de la tarea *easytask*

La lista de alumnos estara fijada en la ruta './students' o podras cambiarla mediante el paramentro **--students**.

![](http://i125.photobucket.com/albums/p79/NooK1e_RG/gitbook/clone_zps6mj10ifh.png)

Podemos ver como se va realizando un push a cada repository para luego comprobar en github que el contenido ha sido correctamente subido a cada tarea.

##Clonar un repositorio de una tarea
`teachers_pet clone_repos`

Si queremos clonar un repositorio en una maquina local usaremos este comando en el que le asignaremos el repositorio de la tarea de los estudiantes que nos interese.

`--repository` Cuando se asigna un repositorio a un usuario, automaticamente se toma como nombre el nombre de del usuario mas el nombre del repositorio original. El nombre que demos utilizar es el de la tarea del repositorio.

En nuestro caso clonaremos los repositorios de la tarea que creamos anteriormente, *easytask*.
```bash
$> teachers_pet clone_repos --organization=classroom-testing --repository=easytask

```
Este comando haria que se clonasesn los repositorios asignados a la lista de alumnos en la direccion actual donde se encuentre la consola de comandos. 

![](http://i125.photobucket.com/albums/p79/NooK1e_RG/gitbook/cloning_zpsqenidgzr.png)

##Abrir un issue para todos los repositorios de la organizacion

`teachers_pet open_issue`

##Añadir colaboladores a un repositorio
`teachers_pet add_collabolators`

Podemos añadir un colabolador a cualquier persona que ha realizado un fork de tu repositorio.

##Hacer un Merge de todos los Pull Requests disponibles en un repositorio
`teachers_pet merge_pull_requests`

##Ver quien ha hecho un fork de un repositorio

`teachers_pet fork`

Con este comando podras saber que alumnos han hecho un fork de un repositorio en concreto, que sea pasado como parametro. La lista de alumnos sera creada y guardada en un archivo students.csv por defecto, o indicando la ruta y el archivo donde quieras con el parametro --output.

