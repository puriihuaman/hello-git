# Git

## Inicializar un repositorio de un proyecto
Dentro del proyecto ejecutamos el siguiente comando:
```
git init
```
## Ramas (Branch)
### ¿Qué es un rama?
Es una copia identica de la rama principal (main|master) hasta el último commit realizado.
Una rama siempre proviene de otra rama, es como un árbol en la vida real una rama sale de otra.
En la rama principal mantenemos los commits principales el cual se subirar a producción en un app.
Las ramas se puede unir a la principal a esto se le denómina **merge**.

Las ramas se les puede nombrar:
* Rama main(mater | main)
* Rama development: "Para desarrollar o experimentar nuevas funcionalidades"
* Rama hotfix: "Para arreglar bug de producción"
---
+ Renombrar la rama por defecto al inicalizar un repositorio:
```
git branch -m <new_branch_name>
```
+ Crear una rama:
```
git branch <branch_name>
git switch -c <branch_name>
```

+ Moverse entre ramas:
```
git switch <branch_name>
```
+ Moverse entre dos ramas previamente visitadas:
```
git switch -  
```
+ Fusionar ramas (main <- develop [traemos los cambios de develop a main]) :
```
git merge <branch_name>
```
+ Eliminar una rama:

Recuerda que cuando se elimina una rama ya no podremos acceder a ella, pero sus commits de la rama eliminada queda 
  en el historial de git (proyecto), al cual podemos acceder mediante los hash(id del commit). 
```
git branch -d <branch_name>
```

## Estado de archivos
```
git status
```
## Agregar al area de fotográfia (staging area)
Agregar archivo por archivo:
```
git add <file>
```
Agregar todos lo archivos que no estan en el area (staging area):
```
git add .
```

## Commit
### ¿Qué es un commit?
Es tomar una instantanea (fotográfia) del estado actual en el que se encuentra tus archivos (proyecto).

Para hace un commit:
```
git commit -m "description"
```

## Historial de commit (Log)
Muestra los commit que vamos realizando de nuestros archivos (proyecto).
Esto los identifica con hash(Combinación de letras y números), este es único para cada commit que se va realizando 
en el proyecto.

Para mostrar el historial de commits del proyecto:
```
git log
```
Ver el historial de una forma mas visual:
```
git log --graph
```

Ver el historial de forma resumida y visual:
```
git log --graph --pretty=oneline
```

Ver el historial de forma resumida:
```
git log --oneline
```
Ver historial completo de todos los commits:
```
git reflog
```

## Moverse entre commits
```
git checkout <hash [id del commit]>
```

## Alias
+ Crear un alias para evitar escribir el comando completo del log:
```
git config --global alias.name_alias "log --graph --pretty=oneline"
```
+ Para usar el alias:
```
git name_alias
```

## Mostrar cambios
+ Muestra que cambios nuevos se agregaron a que archivo y que se elimino:
```
git diff
```

+ Mostrar que cambios hay entre ramas:
```
git diff <branch_name>
```

+ Mostrar que cambios hay entre ficheros:
```
git diff <file_name>
```

## Resetear cambios
+ Moverse a un punto concreto de la rama actual: 
```
git checkout <file>
```
+ Resetear cambios no guardados, vuelve al último commit de la rama actual:
```
git reset
```
+ Volver a un punto(commit) concreto de la rama actual fuerza para volver a ese punto, "casi perdiendo el resto de 
  commit":
+ **Recuerda**: Git guarda en un historial todos los commit realizado a donde se puede volver, para ver usa <git 
  reflog>:
```
git log --hard <hash [id del commit]>
```
## Tag
Hace referencias a etiquetas.
Lo usamos para referenciar puntos importantes, como para las versiones de app.
Para nombrar los tags se recomienda hacerlo en minúsculas, y por lo mucho guiones bajos.

+ Para crear un tag:
```
git tag <tag_name>
```

+ Para mostrar los tag:
```
git tag
```

## Stash
Área temporal, aquí puede guardar cambios temporales que luego puede recuperar e eliminar mientras te mueves entre 
ramas.
Esto se usamos para cuando no queremos hacer commits de cambios simples.

+ Para crear un stash:
```
git stash
```

+ Para mostrar todos los stash:
```
git stash list
```

+ Para recuperar un stash:
```
git stash pop
```

+ Para eliminar un stash: 
```
git stash drop
```

## Sincronizar repositorio local con el remoto 
+ Agregamos al repositorio remoto:
```
git remote add origin <url_repository>
```
+ Para subir cambios:
```
git push origin <main_branch_name>
```
+ 
