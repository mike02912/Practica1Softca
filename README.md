# Practica1Softca

**Primero debemos tener en claro los comandos usados en linux o terminal Bash que son los siguientes**

-pwd
-ls
-cd
-rm
-mkdir
-touch

**Luego proceremos a resolver cada uno de los puntos pedidos en la practica**

## Crear repositorio

> 1. Crear un repositorio en vuestro GitHub llamado Practica1Softca
Realizamos la creación del repositorio en [Github](https://github.com/mike02912/Practica1Softca)

> 2. Clonar vuestro repositorio en local.
Para clonar el repositorio procedemos a usar el siguiente comando

```
git clone git@github.com:mike02912/Practica1Softca.git
```

## README

> 3. Crear (si no lo habéis creado ya) en vuestro repositorio local  un documento README.md.
```
touch README.md
```

## Commit inicial
> 4. Añadir al README.md los comandos utilizados hasta ahora y hacer un commit inicial con el mensaje commit inicial.
```
> git add README.md
> git commit -m "commit inicial"
```

## Push inicial
> 5. Subir los cambios al repositorio remoto.
Comprobemos que esta conectado remoto
```
> git remote -v
```

Luego realizamos la subida de datos al repositorio

```
> git push origin master
```

## Ignorar archivos
> 6. Crear en el repositorio local un fichero llamado privado.txt.
```
touch privado.txt
```
> 7. Crear en el repositorio local una carpeta llamada privada.
```
mkdir privada
```
> 8. Realizar los cambios oportunos para que tanto el archivo como la carpeta sea ignorada por git.
para realizar los cambios debemos crear un archivo llamado `.gitignore`
```
touch .gitignore
```

accedemos y procedemos a agregar aquellos ficheros que queremos omitir (privado.txt , privada)
```
code .gitignore
```

## Añadir fichero 1.txt
> 9. Añadir fichero 1.txt al repositorio local.
```
touch 1.txt
```
## Crear el tag v0.1
> 10. Crear un tag v0.1.
para crear el tag procedemos a ver los cambios dentro del proyecto y elegiremos una version funcionando
```
git log --all
git tag -a v0.1 -m "Creacion del tag v0.1" 
git log --all
```


## Subir el tag v0.1
> 11. Subir los cambios al repositorio remoto.
```
git push origin --tag
```
## Crear una rama v0.2
> 12. Crear una rama v0.2.
```
git branch v0.2
```
> 13. Posiciona tu carpeta de trabajo en esta rama.
```
git checkout v0.2
```
## Añadir fichero 2.txt
> 14. Añadir un fichero 2.txt en la rama v0.2.
```
touch 2.txt
git add 2.txt
git commit -m "Fichero 2 agregado"
```
## Crear rama remota v0.2
> 15. Subir los cambios al repositorio remoto.
```
git push origin v0.2
```
> 16. Posicionarse en la rama master.
```
git checkout master
```
## Merge directo
> 17. Hacer un merge de la rama v0.2 en la rama master.
Desde la rama master, realizar un merge de la rama v0.2
```
git merge v0.2
```

## Merge con conflicto
> 18. En la rama master poner Hola en el fichero 1.txt y hacer commit.
```
code 1.txt
git commit -am "Palabra Hola agregada"
```
> 19. Posicionarse en la rama v0.2 y poner Adios en el fichero "1.txt" y hacer commit.
```
git checkout v0.2
code 1.txt
git commit -am "Palabra Adios agregada"
```
> 20. Posicionarse de nuevo en la rama master y hacer un merge con la rama v0.2
```
git checkout master
git merge v0.2 
```
## Listado de ramas
> 21. Listar las ramas con merge y las ramas sin merge.
Para ver el listado de las ramas que se realizaron merge y aquellas que no
hay 2 maneras, la primera es la usar el comando git log, la primera es la
siguiente:
```
git log --all --graph --decorate --oneline
```

## Arreglar conflicto
> 22. Arreglar el conflicto anterior y hacer un commit.
Arregle el conflicto usando Visual Studio Code y elegir una de las 3 opciones:
ambas o una de los opciones de cada rama.

otra forma es usando el comando desde la terminal 
```
git mergetool
```

## Borrar rama
> 23. Crear un tag v0.2
```
git tag -a v0.2 -m "Creacion del tag v0.2" 
```
> 24. Borrar la rama v0.2
para borrar la rama de nuestro repositorio local:

```
git branch -d v0.2
```

para borrar del repositorio remoto:

```
git push origin --delete v0.2
```
## Listado de cambios
> 25. Listar los distintos commits con sus ramas y sus tags.
para listar los commints con sus ramas y tags podemos utilizar el seguiente comando 
```
git log --oneline
```
