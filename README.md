# DF-MSc-Thesis-LaTeX-template
LaTeX template para la tesis de grado en ciencias fisicas del DF, FCEN, UBA.


## Algunos comentarios utiles:

### Main project file

El archivo principal de proyecto es el `tesis.tex`.

### Makefile

El proyecto ya incorpora una `Makefile` que usa `latexmk`, lo que garantiza que los archivos de proyecto sean procesados el numero de veces necesario y en el orden correcto (incluyendo la generacion de bibliografia e indices) para dar un PDF en caracter final. 

Si se usa desde linea de comandos, haciendo `make help` se accede a una ayuda que detalla los comandos posibles y sus funciones.

Si se emplea TeXShop para compilar/procesar el archivo es posible generar un "engine" de TeXShop que corra ese mismo makefile. En breve pondre aqui mas detalles de como hacerlo.

### Estilo DF-MSc-titlepage

Este proyecto incorpora un archivo de estilo `DF-MSc-titlepage.sty` que permite generar facilmente la portada/caratula de la tesis siguiendo los requerimientos de la catedra de Tesis de Licenciatura del DF, FCEN, UBA. El paquete incluye la posibilidad de usar el logo de la uba, cosa que es posible invocando la opcion `usarlogouba` al llamarlo empleando `\usepackage`.

### Paquete aas_macros.sty

Este paquete se incorpora al proyecto para proveer las definiciones de abreviaturas comunmente encontradas en los archivos `bibtex` que se descargan de los sitios web de origen (abreviaturas como `ApJ`, `JFM`, etc.). Se provee el archivo `.sty` para hacer que este repositorio sea autocontenido, evitando tener que descargarlo en forma independiente. Aprovecho para mencionar explicitamente que no soy autor del paquete `aas_macros.sty`, cuya ultima version puede conseguirse en linea en el sitio de la ADS ABS Harvard.

### Encoding: UTF-8

Conviene usar UTF-8 como encoding para los archivos .tex, esto garantiza que los acentos (y otros caracteres especiales) ingresados en los archivos fuente sean bien incorporados al PDF resultante. Los archivos de este proyecto ya usan ese encoding. Hay que tener cuidado de, al editar estos archivos, no modificar involuntariamente el encoding. Por esto, resulta altamente recomendable fijar, en el procesador de textos utilizado, el encoding en 'UTF-8'.

### Directorio de figuras

Para que funcione correctamente el procesado, es necesario crear una carpeta llamada `figures` en el mismo directorio donde se encuentran los archivos fuente, y poner en esa carpeta todas las imagenes que se deseen luego incluir en la tesis.

### Directorio "auxfiles"

Al procesar el archivo principal del proyecto, el mismo crea un directorio llamado `auxfiles`
 en el mismo directorio donde se encuentran los archivos fuente. En ese directorio se albergan todos los archivos auxiliares intermedios que brinda el procesado, incluyendo logfiles, etc. La idea es que el directorio donde se encuentran los archivos fuente (los `*.tex`) se encuentre siempre libre de esos files que complican la navegacion, sobre todo desde la linea de comandos. 
 
