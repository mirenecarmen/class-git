## CLASE 11 MIÉRCOLES 12 DE JUNIO DEL 2024 
Resolución de conflictos al hacer merge 

Sección lectura

Git nunca borra nada, a menos que nosotros se lo indiquemos. Cuando usamos los comandos git merge o git checkout estamos cambiando de rama o creando un nuevo commit, no borrando ramas ni commits (recuerda que puedes borrar commits con git reset y ramas con git branch -d).

Git es muy inteligente y puede resolver algunos conflictos automáticamente: cambios, nuevas líneas, entre otros. Pero algunas veces no sabe cómo resolver estas diferencias, por ejemplo, cuando dos ramas diferentes hacen cambios distintos a una misma línea.

Esto lo conocemos como conflicto y lo podemos resolver manualmente. Solo debemos hacer el merge, ir a nuestro editor de código y elegir si queremos quedarnos con alguna de estas dos versiones o algo diferente. Algunos editores de código como Visual Studio Code nos ayudan a resolver estos conflictos sin necesidad de borrar o escribir líneas de texto, basta con hacer clic en un botón y guardar el archivo.

Recuerda que siempre debemos crear un nuevo commit para aplicar los cambios del merge. Si Git puede resolver el conflicto, hará commit automáticamente. Pero, en caso de no pueda resolverlo, debemos solucionarlo y hacer el commit.

Los archivos con conflictos por el comando git merge entran en un nuevo estado que conocemos como Unmerged. Funcionan muy parecido a los archivos en estado Unstaged, algo así como un estado intermedio entre Untracked y Unstaged. Solo debemos ejecutar git add para pasarlos al área de staging y git commit para aplicar los cambios en el repositorio.

_Cómo revertir un merge Si nos hemos equivocado y queremos cancelar el merge, debemos usar el siguiente comando:_

* git merge --abort

Conflictos en repositorios remotos Al trabajar con otras personas, es necesario utilizar un repositorio remoto.
­
-Para copiar el repositorio remoto al directorio de trabajo local, se utiliza el comando git clone , y para enviar cambios al repositorio remoto se utiliza git push.

-Para actualizar el repositorio local se hace uso del comando git fetch, luego se debe fusionar los datos traídos con los locales usando git merge.

Para traer los datos y fusionarlos a la vez, en un solo comando, se usa git pull.

­- Para crear commits rápidamente, fusionando git add y git commit -m "", usamos git commit -am "".

­- Para generar nuevas ramas, hay que posicionarse sobre la rama que se desea copiar y utilizar el comando git branch .

Para saltar entre ramas, se usa el comando git checkout

­- Una vez realizado los cambios en la rama, estas deben fusionarse con git merge.

El merge ocurre en la rama en la que se está posicionado. Por lo tanto, la rama a fusionar se transforma en la principal.
Los merges también son commits.
Los merges pueden generar conflictos, esto aborta la acción y pide que soluciones el problema manualmente, aceptando o rechazando los cambios que vienen.

_Repasa qué es un branch_

Sección Práctica

git checkout segunda #falta lo que cargamos en master

git merge master #traemos los cambios desde la master y tenemos las dos ramas actualizadas

Ahora vamos a crear un conflicto para ver como salimos de el, vamos a cargar datos nuevos creando archivos html y css estando en la rama segunda, y también vamos a hacer lo mismo estando en la master y veremos como lo solucionamos.

Abrimos el html y modificamos estando en la rama segunda

Luego commiteamos en la rama segunda y pasamos a la rama master, guardar y commitear, hacer un merge estando en master: pongo en orden los comandos abajo.

* ctrl + s #Guardamos los cambios en la rama segunda, ponemos cambios en css
* git commit -am "Modifique el css y el color del texto" es un ejemplo
* git checkout master #Modificamos el html, ponemos código y css ponemos texto blue
* ctrl + s #Guardamos los cambios
* git commit -am "Agregue suscripción, cambie el código y puse todo azul en css"
* git merge segunda #Hacemos un merge estando en master y veremos el conflicto

Para solucionar el conflicto podemos abrir el archivo con el editor de texto y modificar lo que nos este señalando y guardamos, esto en el css y en el html, lo podemos hacer desde VSC seleccionando: el cambio entrante.
Debemos ahora commitear estos cambios, abajo pongo los comandos.

* git status
* git commit -am "Solución de conflictos al mergear las ramas"
* git checkout segunda #Seguiremos con la versión anterior, porque el merge fue en master
* git merge master #Ahora pasamos los cambios a la rama segunda.

