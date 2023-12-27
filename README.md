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

## Alias
Crear un alias para evitar escribir el comando completo del log:
```
git config --global alias.name_alias "log --graph --pretty=oneline"
```
Para usar el alias:
```
git name_alias
```

## Resetear cambios
Moverse a un punto concreto: 
```
git checkout <file>
```
Resetear cambios no guardados al último commit:
```
git reset
```
