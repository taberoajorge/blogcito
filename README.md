- Incluir dir/file cambios en un repo→```vim
git add [file or path]
```
- Remover file del track en el repo→```vim
 git rm --cached [file]
```
- Remover cambios en un archivo del track en el repo→```vim
 git restore --staged [file]
```
- Comparar stagging vs directorio→```vim
git diff
```
- Resetear los cambios sin borrar lo que hay en staging→```vim
git reset [commit index] --soft
```
- Resetear los cambios forzado→```vim
 git reset [commit index] --hard
```
- Ver los cambios de un dir/file→```vim
git log [dir/file]
```
- Ver los cambios especificos de un dir/file→```vim
 git log [dir/file] --stat
```
- regresar a una version anterior→```vim
 git checkout [commit index] 
```
- Que sucede cuando hago git checkout→La ejecucion de este comando me permite traer una version especifica de un archivo/directorio
- Hice git checkout cuál son las advertencias→Los cambios que trajiste está en el stagging, Si haces commit ese viaje que hiciste pasaría a ser el último cambio de la rama main, si aún no he hecho el commit entonces puedo deshacer el cambio haciendo un checkout de la cabeza del repo(último commit)
- git merge→une los cambios de una rama, a otra.
- Si hago merge a otra rama estando en main, que sucede?→Trae los cambios de la otra rama y los fuciona
- Git fecth + Git merge =→```vim
 git pull [origen]
```
- ```vim
git remote add [name] [url]
```→Para agregar el origen es decir, a donde haremos push/pull
- mostrar arbol de commits, y ramas→```vim
git log --all --graph --decorate --oneline
```
- anadir un tag→```vim
 git tag -a [name del tag] -m "mensaje del tag" [id del commit]
```
- git tag→{{ comando }}  -a v0.0.1 → {{ nombre del tag }}   -m "Primeras clases del curso"→{{ Mensaje del commit }}  269881d →{{ id del comit }}
- Ver el arbol de cambios→```vim
git log --all --graph --decorate --oneline
```
- Ver cual es la referencia del commit desde las etiquetas→```vim
git show-ref ‒-tags
```
- 
- darle acceso a alguien al repo→settings del repo
- Como hacer un pull request→hay dos casos para hacer un pull request, el primero es cuando la rama main esta bloqueada (lo ideal y normal en un project), y cuando haz c reado un fork de un project
- Pertenezco al project de mi organizacion, quiero meter cambios, que hago?→si estoy dentro del project puedo crear una rama, hacer los cambios y solicitar el pull desde github
- Si quiero hacer un fork, lo hago desde github, para tener un instancia propia del project→Aqui para meter cambios lo que tengo que hacer es crear un pull desde github, y solicitar el review de algui y que el DEVOPS apruebe la contribucion
- Inconveniente de ser un contribuidor fuera del project→es que debes estar atento a los cambios del repo original, esto lo puedes hacer viendo desde la interfaz de github, y creando un  origen upstream(este es basicamente la direccion del repo original) donde puedes hacer el push para que los cambios se vaya a tu repo local
- 
- Estructura del commit 
    - commit {{3a8470a616afb8cde8c791b5020346b948c13ee2}} {{Tag, id de commit }} {{(HEAD -> master)}} 
        - Author:{{ taberoajorge <taberoajorge@pm.me>}} {{Autor  }} 
        - {{Date:   Mon Nov 8 19:37:02 2021 -0600 }}  {{ Fecha del commit }} 
        - Se agrega unas lineas al final, que no tienen sentido→Mensaje del commit
    - 
    - 
- Crear un repo
    - En una web→Donde esta el index.html
    - En una app→Donde está la carpeta principal de archivos
    - Crear un repositorio→```vim
 git init [directory]
```
- 
- Conectar Github
    - Crear tu llave ssh→```vim
 ssh-keygen -t rsa -b 4096 -C "email"
```
    - ```vim
eval $(ssh-agent -s) 
```→Evaluar si el servicio de shh esta activo
    - Establece tu email global→```vim
git config --global user.email [email]
```
    - Establecer el nombre de usuario→```vim
 git config --global user.name [name]
```
    - Una vez creada necesitas añadir la llave a tu identidad local→```vim
ssh-add [path donde esta la llave]
```
    - 
- Ver estado del directorio 
    - Ver estado de un dir/file→```vim
 git status [path or file]

```
- Enviar cambios al repositorio
    - Enviar un commit con mensaje→```vim
git commit -m "this is a message"
```
- 
- Ver los cambios en un archivo
    - Ver los cambios en un archivo→```vim
git show [file]
```
    - 
- 
- Ver diferencias de entres dos commits
    - Ver diferencias entres dos commits→```vim
 git diff [commit id] [commit id]
```
- 
- Estados en un repositorio
    - Modified→Cuando se hace una modificacion
    - Untracked→Cuando se agrega un archivo
    - In staging→cuando se da git add
    - In repo→Cuando se envia el commit
- 
- Git workflow 
    - Gitworkflow→es la forma de delegar por ramas
    - Traerme los cambios del repo local→git checkout
    - Flujo normal de git→main, development, hotfix
    - 
- Crear un nueva rama 
- crear una nueva rama→```vim
git branch [name]
```
- Renombrar la rama principal→```vim
 git branch -M [name]
```
- 
- 