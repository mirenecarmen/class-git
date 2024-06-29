**CLASE 6 MIÉRCOLES 8 DE MAYO DEL 2024**
Volver en el tiempo en nuestro repositorio utilizando reset y checkout parte 6

Ingresamos de la siguiente manera:

_Abrir git bash en Window o la terminal de Linux o de Mac: al abrir Git Bash hacerlo como administrador, en terminal también o usar sudo para permisos especiales._

TAREA -> AGREGAR LOS COMENTARIOS EN LOS COMANDOS, PARA SABER QUE PASA CON CADA UNO.

cd tecnicatura
cd class-git
ls
code .

*git log #Vemos los commit hechos hasta ahora*

Copiar el hash #El número largo que tiene el commit

*git reset hash-nombre-commit #Este nos permite volver a una versión anterior, hay 2 tipos de reset: el duro y el suave*

git status
git add .
git commit -m "Agregamos datos de estudios en historia.txt"
*git config --list #Veremos la configuración que ya hemos hecho con en nombre y email*

*git reset hash-nombre-commit --hard #Es el duro, todo vuelve a su estado anterior, es el más usado, desaparece todo*

*git reset hash-nombre-commit --soft #Este es el suave, lo que tengamos en staging segirá allí
crear un archivo #portafolio.html introducir el código y

touch portafolio.html
*html : 5 #Con esto se carga el código básico de html y modificamos*

ctrl + s #Guardamos
Clic derecho en VSC Open with Live Server para ver en el navegador
git status
ls
ls -al
git add .
git status
**git commit -m "Agregamos el html para nuestro portafolio"**
*creamos CSS #Este es un archivo de estilos, para esto creamos una nueva carpeta llamada css*

mkdir css
ls
cd css
touch style.css #creamos un archivo dentro: estilos.css le cargamos el código.

ctrl + s #abrimos en el navegador y todo esta allí, pero todo esto supuestamente en git no existe.

git status #tenemos cosas en el área de trabajo, en staging distintas
git diff + enter #y nos muestra los cambios en memoria ram y en disco
git add . #Agregamos todo al staging
git status #Ya esta todo en memoria ram, a git solo le importan los archivos, guarda las carpetas como rutas y automaticamente las crea

**git commit -m "Creamos el css para darle algo de estilo a nuestro portafolio"**
git log #vemos lo nuevo que hemos hecho sin lo que borramos con el reset fuerte

hacer cambios en historia.txt #Cambiamos la última línea y

ctrl + s 
git diff
git commit -am "cambio en la última línea del historia.txt"
git log

q  #Esto para salir

git log --stat #veremos los cambios especificos que hicimos en cuales archivos por medio del commit y veremos los cambios en bits

q #salimos de la línea de commits, ahora queremos ver como era originalmente el archivo, osea la primera versión, copiamos el nombre del primer commit

git checkout hash-nombre-commit historia.txt #Veremos el archivo en su estado original

git status #Nos sugiere hacer un commit, si lo hacemos borramos todo lo que hicimos antes, debemos seguir con el siguiente commando

git checkout master historia.txt #Volvemos a la versión master del archivo historia.txt, esto es muy peligroso

git checkout hash-nombre-commit historia.txt #Volvemos a hacer esto y cambiamos cosas del archivo

git commit -am "Reemplazo de una versión por otra de la historia"

git log #Veremos los cambios sin tocar ningun otro archivo, esta es la forma de volver a una versión hacía atrás y llevarla a la cabeza de la master

cd ..

cd ..



La tarea de hoy, agregar esta clase al README.md con el lenguaje de markdown, como lo hicimos en la clase pasada, luego deben hacer el commit correspondiente al cambio agregado.