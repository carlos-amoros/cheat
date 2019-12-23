Github
======

Como comenzar: [Hello World](https://guides.github.com/activities/hello-world/)

## 1. Crear repositorio
* En el icono + -> Crear nuevo repositorio
## 2. Crear una rama
* La rama ```master``` es la principal. 
* Haciendo click en el desplegable ```Branch: master``` podemos crear una nueva rama
## 3. Hacer un commit
* Hacer un commit es salvar un cambio
* Podemos editar el fichero README.md desde la interfaz web. Hacemos un comentario sobre la modificación y hacemos click en ```Commit Changes``` (lo hemos hecho en la rama ```readme-edits```). Ahora esta rama contiene un contenido diferente de la ```master```.
## 4. Abrir una Pull request
* Cuando se abre una pull request se está proponiendo que los cambios realizados sean revisados por alguien y los fusione (merge) en una rama. Abrir pull request con nosotros mismos carece de sentido, pero sirve para aprender el funcionamiento de Github.
* Como base dejamos ```master``` y comparamos con ```readme-edits```. Podemos ver las diferencias en el fichero. 
* Hacemos click en ```Create Pull Request```. A continuación vemos el fichero, podemos editar el comentario y finalizar creando el pull request. 
* Para finalizar podemos hacer Merge haciendo click en el botón correspondiente. Podemos incluir un comentario explicativo.
* Obtenemos el mensaje ```Pull request successfully merged and closed```. Aparece la opción de borrar la rama si no vamos a usarla más. 

[GitFlow](https://guides.github.com/introduction/flow/)

## Usando la línea de comandos

[Set Up Git](https://help.github.com/articles/set-up-git/)

* 1. Descargar e instalar la última versión de Git: https://git-scm.com/downloads
* 2. Configurar el username en git:
    * ```git config --global user.name "Nombre Usuario"```
    * Confirmación: ```git config --global user.name```
* 3. Configurar la cuenta de correo
    * ```git config --global user.email "usuario@dominio"```
    * Confirmación: ```git config --global user.email```


* Clonar un repositorio: ```git clone repositorio```
    * ```cd /home/camoros/Documentos```
    * ```git clone https://github.com/carlos-amoros/cheat```
    * Esto me crea del directorio ```/home/camoros/Documentos/cheat```
    * ```cd cheat```
    * ```git status```
* Añadir a git todos los cambios hechos en local
    * ```git add .```
* Ejecutar un commit explicando los cambios
    * ```git commit -m "cambios realizados"```
* Subir los cambios
    * ```git push origin master```
* Si tenemos el mismo repositorio en dos dispositivos y queremos actualizarlo en local antes de modificar:
    * ```git pull origin master```

* [Gittutorial](https://git-scm.com/docs/gittutorial)
* [Guía Sencilla](http://rogerdudler.github.io/git-guide/index.es.html)
