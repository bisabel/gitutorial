Comandos basicos
================

Configurar mis datos 
--------------------
Para todos los proyectos en mi pc utilizamos el parametro extra --global, sin el afectaria
  git config --global user.name "nombre"
  git config --global user.email "nombre@email.com"
  git config --global core.editor "vim"
Para listar los parametros que tenemos configurados
  git config --global -l
  
Empezar con un proyecto versionado
----------------------------------
Para inicializar un control de versiones en la carpeta que estemos
  git init
Para clonar un proyecto y traernos todo su historico de cambios
  git clone "url"
  
Comprobar la situacion
----------------------
Dentro de una carpeta de un proyecto con git, comprobaremos su estado con
  git status
Para listar el historico de cambios
  git log

Realizando cambios y guardandolos
--------------------------------
He modificado un fichero y lo quiero llevar a staging area
        git add fichero
He creado un nuevo fichero y quiero que git haga seguimiento sobre el
        git add fichero       
Para sacar un fichero del staging area, sin perder las modificaciones que hay en él
  git reset HEAD <fichero>
Para deshacer las modificacions realizadas en un fichero  
  git checkout -- <fichero>        
  
Quiero guardar los cambios que tengo en el staging area. creando un nuevo puento en el historico del proyecto.
  git commit -m "mensaje descriptivo de los cambios que contiene"



