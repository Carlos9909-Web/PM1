# Comandos para el examen 

## Iniciar repositorio
git init
git add .
git commit -m"commit inicial"
![commit](imagenes/primercommit.png)


## Ignorar archivos

Crear archivo .gitignore y poner: 
privado/
privado.txt
![gitignore](imagenes/gitignore.png)

## Crear tag
* Para ver el nombre del commit:
git log --oneline

* Crear el tag:
git tag -a v0.1 -m"Primer Tag" dc72066
![Tag](imagenes/tag.png)


## Creacion de ramas
* Crear rama y posicionarte en ella:
git checkout -b "v0.2"
![Ramas](imagenes/creacion%20de%20ramas.png)


## Merge directo
* Posicionarse en la rama master
git checkout master

* Hacer un merge de la rama v0.2 en la rama master. 
git merge v0.2
![Merge Directo](imagenes/conflicto.png)

## Merge con conflicto 
* En la rama master poner Hola en el fichero 1.txt y hacer commit. 
//Modificar el archivo
git add archivo1.txt
git commit -m"Cambio"
* Posicionarse en la rama v0.2 y poner Adios en el archivo "1.txt" y hacer commit. 
git checkout v0.2
//Modificar el archivo
* Posicionarse de nuevo en la rama master y hacer un merge con la rama v0.2 
git checkout master
git merge v0.2
![Conflicto](imagenes/conflicto.png)


# Listado de ramas 
* Listar las ramas con merge y las ramas sin merge. 
git branch -v
![Listado de ramas](imagenes/listado%20de%20ramas.png)

## Arreglar conflicto 
* Arreglar el conflicto anterior y hacer un commit. 
//Aceptar el primer cambio "Hola"
git add archivo1.txt
git commit -m"Solucion de conflicto" 

## Borrar rama 
* Crear un tag v0.2 
git tag -a v0.2 -m"v0.2" 3cbd0d6
* Borrar la rama v0.2 
git merge -d "v0.2"
 

## Listado de cambios 
* Listar los distintos commits con sus ramas y sus tags.
git log --graph --all --oneline
![Listado de imagenes](imagenes/listado%20de%20cambios.png)
