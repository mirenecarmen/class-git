# CLASE 5 MIÉRCOLES 24 DE ABRIL DEL 2024

**¿Qué es el staging?**

_Tienes una carpeta donde están los archivos de tu proyecto o un directorio y allí tenemos el archivo historia.txt, cuando entramos por consola a ese archivo y creamos el git init, se crea un área en memoria ram que se llama staging, y el otro es el repositorio esta es la carpeta .git donde estarán todos los cambios al final del proyecto.

Entonces tenemos el área de trabajo, cuando colocamos git add historia.txt pasamos al staging o área de preparación, que hay que recordar que esto es en la memoria ram y luego con git commit -m "Mensaje" pasa al repositorio en la rama master, allí se genera un nombre llenos de letras y números, es el hash, el nombre del commit._

**¿Qué es Gitflow?**

_Gitflow es un modelo alternativo de creación de ramas en Git en el que se utilizan ramas de función y varias ramas principales. Fue Vincent Driessen en nvie quien lo publicó por primera vez y quien lo popularizó._

**¿Qué es branch (rama) y cómo funciona un merge en git?**

_Tenemos una rama llamada master y es donde están los cambios de nuestros archivos, con cada commit creamos una nueva versión

Vamos a crear una rama experimental para otras versiones que suele llamarse development, al encontrar bug, se crea otra rama que suele llamarse hotfix para hacer reparaciones, siempre que ya tengamos resultados favorables, es donde decidimos hacer un merge, es unir los resultados de las ramas a la rama master.

La principal característica de las ramas principales es que solo existe una de cada tipo. El objetivo es que no se instancien y que no reciban código de forma directa a través de commit, siempre tienen que recibir código a través de ramas de tipo Feature, Release y Hotfix, siempre a través de ramas auxiliares.

Es un riesgo recibir código directamente en la rama Master, porque puede generar defectos en el repositorio en las subidas a producción, que no contemplemos o que no preveamos, por lo que siempre es mejor integrar código en otras ramas antes de integrar con las ramas Master y Develop.

Esta es una metodología estricta pero que da lugar a diferentes interpretaciones o diferentes formas de llevarla en cada equipo, por lo que en algunos casos, algún experto puede permitirse no seguir esa norma, pero son casos muy específicos y siempre de personas de confianza.

En las ramas auxiliares tenemos la rama Feature, la rama Release y la Rama Hotfix, que puede instanciarse todas las veces que se consideren necesarias:

La rama Feature, para nuevas características, nuevos requisitos o nuevas historias de usuario.
La rama Release, para estandarizar o cortar una serie de código que ha estado desarrollándose en la rama Develop, se saca una rama de este tipo, se mergea y ahí se depura.
La rama Hotfix, que habitualmente se utiliza para código para depurar el código que venga de producción, por haberse detectado un defecto crítico en producción que deba resolverse, al que se le va a hacer una Release puntual para corregirlo.
Estas ramas tienen un principio y un fin, ya que son ramas que se mergean con las ramas Master y Develop y desaparecen.


Podemos tener tantas ramas como queramos, tantos repositorios como queramos, lo más importante es saber cuando hacemos un merge, porque es posible que hayan archivos que rompan otros archivos, a esto se lo llama conflicto o bug._

