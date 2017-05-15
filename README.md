# Ejecuar_Java_Sublime
Info from http://ayudasprogramacionweb.blogspot.com.es/2012/12/compilar-y-ejecutar-java-desde-sublime-text.html

Instrucciones:
En esta entrada veremos como configurar un llamado Build System de Sublime Text para que al presionar ctrl + b se 
compile y ejecute nuestra aplicación en JAVA.

Lo primero que debemos hacer es iniciar Sublime Text, una vez lo hallamos hecho, vamos a Tools -> Build System -> 
New Build System... Esto abrirá un pequeño archivo con unas lineas escritas en JSON, de modo que debemos copiar el
siguiente código y pegarlo en este archivo.

	//Codigo valido para Windows y Linux
{
    "cmd": ["javac ${file_name} && java ${file_base_name}"],
    "shell": true
}

Cuando lo hallamos hecho, guardamos dicho archivo en la carpeta donde nos sugiere Sublime Text, y le
ponemos un nombre descriptivo como por ejemplo ejecutarJava.sublime-build, ten cuidado que la extensión del archivo sea 
.sublime-build.

Y con eso ya hemos terminado, para compilar y ejecutar nuestros programas en JAVA tan solo debes ir a Tools -> Build System 
y elegir el nombre del archivo que has modificado antes, en mi caso ejecutarJava. A partir de ahora, podremos compilar y 
ejecutar nuestros programas en JAVA presionando ctrl + b. 
