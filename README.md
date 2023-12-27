# Git

## Inicializar un repositorio de un proyecto
Dentro del proyecto ejecutamos el siguiente comando:
```
git init
```
## Ramas (Branch)
Renombrar la rama por defecto al inicalizar un repositorio:
```
git branch -m nombre_rama
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