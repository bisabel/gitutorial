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
Si queremos traer la informacion de los posibles cambios de un repositorio remoto que hayan podido realizarse
*git fetch <repositorio>* Si no pasamos un nombre, por defecto entiende que es el repositorio origin

Ramificaciones
--------------
Si queremos listar las ramas de trabajo de nuestro repositorio
*git branch*
En el listado, aparecera un * para indicarnos en la rama en la que estemos situados actualmente
Si queremos que nos liste las ramas de nuestro repositorio local, y el de los repositorios remotos.
*git branch -r*
Para crear una nueva rama de trabajo y posicionarnos en ella
*git branch <nombre>*




