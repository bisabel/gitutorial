Comandos basicos
================

Configurar mis datos 
--------------------
Para todos los proyectos en mi pc utilizamos el parametro extra --global, sin el afectaria

*git config --global user.name "nombre"*

*git config --global user.email "nombre@email.com"*

*git config --global core.editor "vim"*

Para listar los parametros que tenemos configurados

*git config --global -l*
  
Empezar con un proyecto versionado
----------------------------------
Para inicializar un control de versiones en la carpeta que estemos

*git init*

Para clonar un proyecto y traernos todo su historico de cambios

*git clone <url>*
  
  
Comprobar la situacion
----------------------
Dentro de una carpeta de un proyecto con git, comprobaremos su estado con

*git status*

Para listar el historico de cambios

*git log*


Realizando cambios y guardandolos
--------------------------------
He modificado un fichero y lo quiero llevar a staging area

*git add <fichero>*
  
He creado un nuevo fichero y quiero que git haga seguimiento sobre el

*git add <fichero>*       
  
Para sacar un fichero del staging area, sin perder las modificaciones que hay en él

*git reset HEAD <fichero>*
  
Para deshacer las modificacions realizadas en un fichero  

*git checkout -- <fichero>*
  
Quiero guardar los cambios que tengo en el staging area. creando un nuevo puento en el historico del proyecto.

 *git commit -m "mensaje descriptivo de los cambios que contiene"*
 

Trabajando con proyectos remotos
--------------------------------
Para ver los repositorios remotos de nuestro proyecto

*git remote -v*

Para añadir un nuevo repositorio remoto 

*git remote add <nombre> <url>*
  
Eliminar la referencia a un repositorio remoto

*git remote rm <nombre>*
  

Ramificaciones
--------------
Si queremos listar las ramas de trabajo de nuestro repositorio

*git branch*

En el listado, aparecera un * para indicarnos en la rama en la que estemos situados actualmente

Si queremos que nos liste las ramas de nuestro repositorio local, y el de los repositorios remotos.

*git branch -r*

Para crear una nueva rama de trabajo, y luego, situarnos sobre ella, usamos los siguientes comandos

*git branch <nombre>*
  
*git checkout <nombre>*
  
O bien, realizar los dos anteriores en uno solo con:

*git checkout -b <nombre>*
  

Enviando y trayendo cambios del servidor
----------------------------------------
Si queremos traer la informacion de los posibles cambios de un repositorio remoto que hayan podido realizarse

*git fetch <repositorio>* Si no pasamos un nombre, por defecto entiende que es el repositorio origin

Si queremos que actualice la carpeta de trabajo que tengamos actualmente con los últimos cambios del servidor:
*git pull <repositorio> <rama>*

Ojo, este comando realiza un fetch

Si queremos enviar bnuestro cambios al servidor:
*git push <repositorio> <rama>*

Ojo, si hay cambios en el servidor que aun no tengamos, no nos dejará hasta que los descarguemos y los juntemos con los nuestros.


Submodulos
----------
Un submodulo nos permitirá tener un proyecto git, dentro de nuestro actual proyecto.

Para crear uno:

*git submodule add <url>*

Cuando realizo un clonado de un proyecto que tiene submodulos (lo puedo mirar en el fichero .gitmodules) no trae los datos del submodulos por defecto, hay que:

*git submodule init*

*git submodule update*


Extra
-----
Si queremos que ignore el seguimiento de archivos y carpetas, lo escribimo en el fichero .gitignore

Para crear disparadores en nuestro proyecto en local, tenemos que utiliza la carpeta .git/hook/ Lo mejor es renombrar un archivos ejemplo existente que trae, y quitarle la extension .sample

Para hacer un guardado rápido de nuestro trabajo, sin que implique commit, podemos utilizar stash

*git stash* para crear un guardado rápido.

*git stash list* para que liste los diferentes guardados que hemos realizado

*git stash apply <id>* para recuperar una situacion de cambios previamente guardada.




