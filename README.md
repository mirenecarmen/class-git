git status

git add .

git status

git commit -m "Cargamos el README dentro del directorio class-git"

git status

git log #Para ver los dos commits hechos: Si tienes commiteada alguna clase anterior veras mas commits de los que yo tengo.

cd ..

cd ..

Sintaxis de escritura y formato básicos
Crear formatos sofisticados para tu prosa y código en GitHub con sintaxis simple.
Encabezados
Para crear un encabezado, agrega entre uno y seis símbolos # antes del encabezado del texto. El número de # que utilices determinará el nivel jerárquico y el tamaño tipográfico del encabezado.

# A first-level heading
## A second-level heading
### A third-level heading
Captura de pantalla de GitHub Markdown en la que se muestran los encabezados h1, h2 y h3 de ejemplo, que descienden en el tamaño de tipo y el peso visual para indicar el nivel de jerarquía descendente.

Al usar dos o más encabezados, GitHub genera automáticamente una tabla de contenido a la que puede acceder haciendo clic en  dentro del encabezado del archivo. Todos los títulos de encabezado aparecen en la tabla de contenido, y puede hacer clic en un título para ir a la sección seleccionada.

Captura de pantalla del archivo LÉAME en el repositorio de código abierto GitHub Docs con el menú desplegable de la tabla de contenido expuesto. El icono de la tabla de contenido aparece en naranja oscuro.

Estilos de texto
Puedes indicar énfasis con texto en negrita, cursiva, tachado, o de subíndice o superíndice en los campos de comentarios y archivos .md.

Estilo	Sintaxis	Métodos abreviados de teclado	Ejemplo	Resultados
Bold	** ** o __ __	Command+B (Mac) o Ctrl+B (Windows/Linux)	**This is bold text**	Esto es texto en negrita.
Cursiva	* * o _ _     	Command+I (Mac) o CtrI+ (Windows/Linux)	_This text is italicized_	Este texto está en cursiva
Tachado	~~ ~~	Ninguno	~~This was mistaken text~~	Este texto está equivocado
Cursiva en negrita y anidada	** ** y _ _	Ninguno	**This text is _extremely_ important**	Este texto es extremadamente importante
Todo en negrita y cursiva	*** ***	Ninguno	***All this text is important***	Todo este texto es importante
Subscript	<sub> </sub>	Ninguno	This is a <sub>subscript</sub> text	Se trata de un texto de subíndice
Superscript	<sup> </sup>	Ninguno	This is a <sup>superscript</sup> text	Se trata de un texto de superíndice
Entrecomillado de texto
Puede entrecomillar texto con >.

Text that is not a quote

> Text that is a quote
Al texto entre comillas se le ha aplicado sangría y tiene un color de tipo diferente.

Captura de pantalla de GitHub Markdown en la que se muestra el texto entre comillas de ejemplo. La comilla tiene sangría con una línea vertical a la izquierda y su texto es gris oscuro en lugar de negro.

Nota: Al visualizar una conversación, puedes citar automáticamente el texto en un comentario resaltándolo y escribiendo R. Para citar un comentario completo; para ello, haz clic en  y, a continuación, en Citar respuesta. Para obtener más información acerca de los métodos abreviados de teclado, consulte "Accesos directos del teclado."

Código de cita
Puedes indicar un código o un comando dentro de un enunciado con comillas simples. El texto dentro de las comillas simples no será formateado. También puedes presionar el método abreviado de teclado Comando+E (Mac) o Ctrl+E (Windows o Linux) para insertar las comillas simples de bloque de código en una línea de Markdown.

Use `git status` to list all new or modified files that haven't yet been committed.
Captura de pantalla de GitHub Markdown en la que se muestra la apariencia de los caracteres rodeados por acentos graves. Las palabras "git status" aparecen en un tipo de letra de ancho fijo, resaltado en gris claro.

Para formatear código o texto en su propio bloque distintivo, usa comillas triples.

Some basic Git commands are:
```
git status
git add
git commit
```
Captura de pantalla de GitHub Markdown en la que se muestra un bloque de código. Las palabras "git status", "git add" y "git commit" aparecen en un tipo de letra de ancho fijo, resaltado en gris claro.

Para obtener más información, vea «Crear y resaltar bloques de código».

Si editas fragmentos de código y tablas con frecuencia, puedes beneficiarte de habilitar una fuente de ancho fijo en todos los campos de comentarios de GitHub. Para obtener más información, vea «Acerca de escritura y formato en GitHub».