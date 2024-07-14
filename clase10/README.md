## CLASE 10 MIÉRCOLES 5 DE JUNIO DEL 2024 - Portafolio 4
Fusión de ramas con Git merge parte 10

La fusión en Git es la forma en que este sistema une un historial bifurcado. El comando git merge permite integrar líneas de desarrollo independientes generadas por git branch en una sola rama. Con este comando, podemos crear un nuevo commit que combina dos ramas o branches: la rama actual y la rama que se indica después del comando.

Estos comandos de fusión del merge afectan solo a la rama actual y no a la rama de destino. Por lo tanto, te recomendamos utilizar git checkout para seleccionar la rama actual y git branch -d para eliminar la rama de destino obsoleta.

#Funcionamiento de Git merge

Git merge fusiona secuencias de confirmaciones en un solo historial, generalmente para combinar dos ramas. Busca una confirmación de base común y genera una confirmación de fusión que representa la combinación de las dos ramas hasta el resultado final.

#¿Cómo unir dos ramas en git?

Ahora bien, para combinar ramas en tu repositorio local, usa git checkout para cambiar a la rama donde deseas fusionar. Por lo general, esta es la rama principal. Luego, emplea git merge y especifica el nombre de la otra rama que deseas traer a esta rama. Ten en cuenta que esto es una combinación de avance rápido.

#¿Cómo realizar un merge en git?

Para hacer un merge en Git, primero asegúrate de estar en la rama correcta. Después, usa el comando git merge seguido del nombre de la rama que quieres combinar. Por ejemplo, si quieres crear un nuevo commit en la rama master con los cambios de la rama segunda, usa este comando:

git checkout master
git merge segunda

Es importante tener en cuenta que en caso de haber conflictos, debes guardar tus cambios antes de hacer git checkout para evitar perder tu trabajo. También es recomendable emplear los comandos básicos de GitHub, como git fetch, git push y git pull, para mantener actualizado tu repositorio.

En este ejemplo, vamos a crear un nuevo commit en la rama master combinando los cambios de una rama llamada segunda: Otra opción es crear un nuevo commit en la rama segunda combinando los cambios de cualquier otra rama:

Git es asombroso porque puede saber cuáles cambios deben conservarse en una rama y cuáles no. En casos de conflictos, asegúrate de guardar tus cambios antes de hacer git checkout para evitar perder tu trabajo.

_Comandos básicos de GitHub:_

* git init # crear un repositorio, si ya esta en la nube traerlo sin hacer git init
* git add . #agregar un archivo a staging.
* git commit -m “mensaje” #guardar el archivo en git con un mensaje.
* git branch nombre_rama #crear una nueva rama.
* git checkout nombre_rama #moverse entre ramas.
* git push origin rama #mandar cambios a un servidor remoto.
* git fetch #traer actualizaciones del servidor remoto y guardarlas en nuestro repositorio local.
* git merge rama #tiene dos usos. Uno es la fusión de ramas, funcionando como un commit en la rama actual, trayendo la rama indicada. Su otro uso es guardar los cambios de un servidor remoto en nuestro directorio.
* git pull origin rama #fetch y merge al mismo tiempo.
* git checkout “codigo de version” “nombre del archivo” #volver a la última versión de la que se ha hecho commit.
* git reset #vuelve al pasado sin posibilidad de volver al futuro, se debe usar con especificaciones.
* git reset --soft #vuelve a la versión en el repositorio, pero guarda los cambios en staging. Así, podemos aplicar actualizaciones a un nuevo commit.
* git reset --hard #todo vuelve a su versión anterior
* git reset HEAD #saca los cambios de staging, pero no los borra. Es lo opuesto a git add.
* git rm #elimina los archivos, pero no su historial. Si queremos recuperar algo, solo hay que regresar. se utiliza así:
* git rm --cached #elimina los archivos en staging pero los mantiene en el disco duro.
* git rm --force #elimina los archivos de git y del disco duro.
* git status #estado de archivos en el repositorio.
* git log #historia entera del archivo.
* git log --stat #cambios específicos en el archivo a partir de un commit.
* git show #cambios históricos y específicos hechos en un archivo.
* git diff “codigo de version 1” “codigo de version 2” #comparar cambios entre versiones.
* git diff #comparar directorio con staging.

# Comando en producción: TUVE QUE SOLUCIONAR UN CONFLICTO

+ git status #En rama segunda: hacemos cambios en el archivo y guardamos
+ git commit -am "Finalizado el cambio en rama segunda" #enter
+ git status
+ git checkout master #perdemos todo lo que ya habíamos hecho, hacemos cambios en el archivo agregando un nuevo parrafo y guardamos
+ git commit -am "Agregado el contenido adicional del archivo y un mejor aporte"
+ git checkout segunda #vemos como desaparecen los cambios
+ git checkout master #Aquí es que vamos a hacer el merge
+ git merge segunda #En mi caso tuve algunos conflictos que solucione a través de VSC, aclaro que nunca debemos utilizar Fusionar los dos cambios
+ git commit -am "Arreglando conflicto" #Una vez solucionado debemos commitear
+ git status #Debemos revisar en el navegador y en el código si algo quedo mal y cambiarlo
+ git commit -am "Solucionado el conflicto 2"
+ git merge segunda #ahora todo va bien
+ git commit -am "Volvi a comentar en este caso de mi area laboral" #Añado información al archivo
+ git log

+ q #Para salir

+ git commit -am "Para guardar estos cambios en el README.md"
+ git checkout segunda
+ git merge master #Traemos todos los cambios
+ git commit -am "Cargamos esto ahora" #vamos a master y mergeamos
+ git checkout master
+ git merge segunda #y terminamos con esto