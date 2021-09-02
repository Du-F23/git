## Manual de comandos para el uso de GIT en linux.
### Elaborado por Fernando Duarte Villavicencio.

##### Contenido recuperado del manual obtenido del enlace [PRO GIT](https://github.com/progit/progit2-es/releases/download/2.1.23/progit.pdf).

Configuracion de la identidad del usuario.

Configuración del nombre de usuario
>`git config --global user.name "Duarte V Fernando DSM 43"`.
![Ejemplo de git help](user.png)

Configuración del correo asociado al usuario
>`git config --global user.email "al222010329@gmail.com"`.
![Ejemplo de git help](email.png)

Si deceamos añadir nuestro editor de codigo por defecto que es de nuestro agrado 
>`git config --global core.editor neovim`.
![Ejemplo de git help](editor.png)

Para verificar que nuestra configuración sea la correcta lo realizaremos mediante el siguiente comando 
>`git config --list`
 ![Ejemplo de git help](config_list.png)
 o si bien deseamos un parametro en especifico usamos
 >`git config "Parametro"` __*cabe resaltar que no se deberian colocar las comillas*__

__*Ejemplo*__
>`git config user.name`.
![Ejemplo de git help](config_parametro.png)

Para obtener ayuda de la gran mayoria de comandos proporcionados por git 
>`git help`. 
![Ejemplo de git help](git_help1.png)
![Ejemplo de git help](git_help2.png)


_______________________________________________________


### Iniciar un repositorio de GIT.

Para iniciar un repositorio en git previamente debimos haber realizado la configuración de usuario
>`git init`.

Para empezar a añadir nuestro trabajo se haria de la siguiente manera
>`git add *` 
![Ejemplo de git help](add.png)
si deseamos añadir todo el contenido dentro de la carpeta, o si bien deseamos solo un contenido en especifico se haria de la siguiente forma 
>`git add "Nombre_documento"` 
__*cabe resaltar que no se deberian colocar las comillas*__.

__*Para que nuestros documentos sean guardados debemos añadir un comentario con los cambios añadidos*__ para ello usaremos 
>`git commit -m "Comentario con los cambios"`

__*Ejemplo*__

`git commit -m "Añadimos todos los archivos". ![Ejemplo de git help](commit.png)

Para clonar contenido de algun repositorio dentro de Github y __*derivados primero debemos obtener la URL*__
>`git clone https://github.com/Du-F23/angular-api.git` ![Ejemplo de git help](clone.png)
O si queremos que se guarde en un directorio con nombre en especifico `git clone https://github.com/Du-F23/angular-api.git nombre_carpeta`
>`git clone https://github.com/Du-F23/angular-api.git Prueba`.
![Ejemplo de git help](clone_carpeta.png).

Para verificar el estado del repositorio
>`git status`.
![Ejemplo de git help](status.png)

Si no queremos que se añadan carpetas o documentos en especifico a el repositorio

>touch .gitignore 
![Ejemplo de git help](gitignore.png)
__*Aqui editaremos el archivo llamado .gitignore y añadiremos las carpetas excluidas por nosotros*__.
![Ejemplo de git help](gitignore_ejemplo.png)

Para eliminar archivos del area de preparación 
>`rm nombre_archivo`

__*Ejemplo*__

`rm indes.html`.

Para renombrar archivos en git 
>`mv nombre_actual nombre_nuevo`

__*Ejemplo*__

`mv arrachera.jpg taco_arrachera.jpg`.

Para ver el registro de confirmaciones 
>`git log`
![Ejemplo de git help](log.png)

Para añadir remote de algun repositorio.
`git remote add origin URL`.

__*Ejemplo*__
>`git remote add origin https://github.com/Du-F23/comandos_git.git`

Para ver todos los repositorios remotos o clonados
>`git remote -v`
![Ejemplo de git help](remote.png)

______________________________________

### Creacion de alias para comandos de git

>`git config --global alias.nombre_alias accion`

__*Ejemplo*__

`git config --global alias.ci commit`
y para mandar a llamar a nuestro alias seria de la siguiente manera
`git ci -m "Creamos un alias"`. 
![Ejemplo de git help](alias.png)

________________________________________

## Ramas en git

### Creacion de una nueva rama

>`git branch -M nombre_rama` 
podemos crear diferentes ramas pero las mas comunes son __*master y main*__.

__*Ejemplo*__ 

`git branch -M master`
![Ejemplo de git help](branch.png)

### Subir rama a repositorio remoto 
>`git push -u origin nombre_rama`

__*Ejemplo*__

`git push -u origin main`
![Ejemplo de git help](push.png)
