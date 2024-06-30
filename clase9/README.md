**CLASE 9 MIÉRCOLES 29 DE MAYO DEL 2024 - Portafolio 3**
*Introducción a las ramas o branches de Git parte 9*

Cuando entramos en el proyecto veremos que nos encontramos con la rama master, y es a partir de allí que debe saber que esta es la rama madre o principal rama, y las otras ramas se crean para no afectar a la master


Las ramas (branches) son la forma de hacer cambios en nuestro proyecto sin afectar el flujo de trabajo de la rama principal. Esto porque queremos trabajar una parte muy específica de la aplicación o simplemente experimentar.

La cabecera o HEAD representan la rama y el commit de esa rama donde estamos trabajando. Por defecto, esta cabecera aparecerá en el último commit de nuestra rama principal. Pero podemos cambiarlo al crear una rama (git branch rama, git checkout -b rama) o movernos en el tiempo a cualquier otro commit de cualquier otra rama con los comandos (git reset id-commit, git checkout rama-o-id-commit).

Repasa: ¿Qué es Git?

Cómo funcionan las ramas en GIT
Las ramas son la manera de hacer cambios en nuestro proyecto sin afectar el flujo de trabajo de la rama principal. Esto porque queremos trabajar una parte muy específica de la aplicación o simplemente experimentar.


git branch nombre de la rama #Con este comando se genera una nueva rama.

git checkout nombre de la rama #Con este comando puedes saltar de una rama a otra.

git checkout -b rama #Genera una rama y nos mueve a ella automáticamente, Es decir, es la combinación de git branch y git checkout al mismo tiempo.

git reset id-commit #Nos lleva a cualquier commit no importa la rama, ya que identificamos el id del tag., eliminando el historial de los commit posteriores al tag seleccionado.

git checkout rama-o-id-commit #Nos lleva a cualquier commit sin borrar los commit posteriores al tag seleccionado.



Vamos a hacer una practica: mientras la rama master esta cambiando normalmente, vamos a crear una rama paralela que va a crear nuevas secciones: osea una sección y a esta rama la vamos a llamar segunda y con esto, la vamos a fusionar para ver como queda en la rama master y así entender el flujo de ramas entre git. Al crear otra rama estamos creando una copia de todos los commit que ya tiene la rama master en la nueva rama y todos los cambios que hagamos en esta nueva rama, no los va a ver la rama master hasta que no la volvamos a fusionar con un proceso que se llama merge.

Abrir terminal #En ubuntu

Abrir como adminstrados git bash #En window

cd Tecnicatura

cd class-git

code . #En ubuntu

code . #En window, abrir como administrador

ctrl + s #Guardamos

clic mouse derecho #Abrimos en el navegador con Live Server vemos los cambios

git status

git commit -am "mensaje del commit" #Este solo funciona con archivos creado previamente

git commit -a -m "Mensaje del commit" #Esto es lo mismo que el anterior

git commit -a + enter #Se abrira el entorno para editar el vim con el mensaje

Escribir el mensaje

ctrl + x

s + enter #No cambiar el nombre ni ruta de ubicación

git log #Veremos los cambios guardados

q #Para salir

git log --stat #Veremos los cambios nombrando cada archivo

q #Para salir

git branch #Muestra en la rama que estamos, desde aquí crearemos una nueva

git show #Muestra el último cambio que hicimos, esto significa que desde el HEAD -> master es que haremos cambios

q #Para salir

ctrl + l #Limpiamos consola

git branch segunda #creamos una nueva rama

git show #Nos muestra ahora que esta en el HEAD -> master, cabecera aquí es donde esta apuntando, es decir el último commit esta pegado a dos ramas distintas, aunque todavía estemos en master

q #Para salir

git status #No hay nada para hacer commit

git chekout segunda #Nos movemos hacía otras ramas, en este caso a segunda, esto no se ve en mac ni en ubuntu, para ver donde estamos hay que ingresar...

git branch #veremos en que rama estamos ubicados o ingresando...

git status #Veremos en que HEAD estamos apuntando

VSC #hacemos cambios que veremos con Nico