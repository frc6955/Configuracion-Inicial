# Tutorial de configuracion de ambiente de desarrollo

En el siguiente tutorial se presentara en detalle los pasos necesarios a seguir para instalar el ambiente de desarrollo minimo para desarrollar software en Los Chilis. Este ambiente incluira los lenguajes Java y Python, librerias basicas y el editor Visual Studio Code. Al finalizar esta instalacion, podras trabajar en cualquiera de los proyectos de la temporada sin mayores problemas.

## 1. Hacer una cuenta en Github e instalar Git

Uno de los principales problemas de los equipos de trabajo es lograr sincronizar adecuadamente el progreso individual de cada miembro. En el area de desarrollo de software, se adopto el sistema de control de version (VCS). Existen muchos tipos de VCS, los mas tipicos siendo Git, Subversion y Mercurial. Nosotros usaremos el sistema Git para controlar y sincronizar archivos. Especificamente, usaremos un servicio online llamado Github (ahora mismo estas leyendo este documento en un repositorio privado en Github), el cual ofrece servidores de Git remotos (Git es la herramienta, Github provee la herramienta de una manera mas sencilla para usar). Este paso consta de tres partes:

### 1.a. Hacer una cuenta en Github

Dirigete a la pagina principal de [Github](https://github.com/) y crea una cuenta. Intenta usar un nombre de usuario sencillo y formal, pues algunas compañias piden ver una cuenta de Github en tu curriculum. Una vez activada tu cuenta, envia un correo a un mentor de programacion para agregar tu cuenta a la organizacion de [Los Chilis](https://github.com/frc6955). Aqui se encuentran todos los repositorios privados donde se desarrollara software durante la temporada.

### 1.b. Descarga Git en tu PC

Para poder ejecutar comandos git en tu computador, necesitas instalar el software adecuado. En los siguientes pasos aprenderas a ejecutar comandos en tu comando de linea, por ende basta con instalar el software por ahora. Para descargar Git para Windows, debes ir al siguiente [link](https://git-scm.com/). En una imagen de un monitor encontraras un boton para descargar el instalador para la version mas reciente de Git. El instalador de Git es relativamente complejo de usar por la gran cantidad de opciones que ofrece. En la opcion de instalador por defecto, selecciona Notepad++ (en caso de que este instalado) ([Notepad++](https://notepad-plus-plus.org/) es un editor de texto extremadamente util por su velocidad y soporte para multiples lenguajes. A pesar de que no se explica en esta guia como instalar, recomiendo fuertemente ingresar a la pagina y descargarlo) o Nano. En la opcion de modificar el ambiente PATH, selecciona la segunda opcion (Git from the command line and also from 3rd-party software). **Este paso es importante**, pues nos va a permitir acceder a Git desde otras herramientas que instalemos. Todas las demas opciones estan bien con la seleccion por defecto, asi que selecciona continuar hasta que se instale el programa.

### 1.c. Lee mas al respecto

Dado que Git es un tema relativamente extenso como para una guia, dejo a continuacion un par de recursos interesantes. El primero se encuentra en este [link](http://anitacheng.com/git-for-non-developers) y es un articulo que presenta Git desde la perspectiva de alguien desentendido en el tema. No te preocupes mucho de los comandos en este primer articulo y enfocate mas en la informacion que se presenta al comienzo. El segundo link es una [respuesta en Quora](https://qr.ae/TUtx8q). Aqui se presenta el funcionamiento de Git mediante los comandos mas basicos y necesarios del programa, ademas el concepto de *branching*. Aqui **si es** necesario leer y entender los comandos que se utilizan, pues representan la gran mayoria de los comandos que usaremos mientras trabajemos.

## 2. Instalar Java

Java ofrece un software llamado *Java Development Kit* (JDK), el cual incluye todo el software necesario para poder desarollar aplicaciones Java. El JDK se encuentra actualmente en su version 11 y se puede descargar desde [este link](https://www.oracle.com/technetwork/java/javase/downloads/jdk11-downloads-5066655.html). En caso que el link no funcione, basta con buscar "JDK download" en Google y buscar un resultado que lleve a la pagina de [oracle.com](https://www.oracle.com/). Una vez abierta la pagina, deberas bajar a la tabla gris que incluye los links de descarga, hacer click en *Accept License Agreement* y descargar el archivo `jdk-11.0.1_windows-x64_bin.exe` (en caso que esta guia no haya sido actualizado, pueden cambiar los numeros, pero basta con seleccionar la descarga ejecutable para Windows). Se debe correr el instalador descargado y apretar Next o Siguiente hasta que se instale el programa.

## 3. Instalar Python

Para poder programar y ejecutar codigo Python, se debe instalar el equivalente a un SDK para Python. Este lo encontraras en el [siguiente link](https://www.python.org). Al poner el mouse sobre el link de Downloads o Descargas, mostrara un boton para descargar Python 3.7.1. Una vez descargado, debes ejecutar el instalador. Antes de apretar instalar, debes seleccionar el recuadro que dice "Add Python 3.7 to PATH". **Este paso es esencial**. Si no se selecciona esa opcion antes de instalar, debes desinstalar el software desde el Panel de Control y luego instalarlo nuevamente, seleccionando dicha opcion. Una vez seleccionado, basta con apretar Install Now para instalar todo.

## 4. Verificar instalaciones

Para verificar todas las instalaciones, debes abrir un comando de linea (terminal). Esto lo puedes lograr de dos maneras:
 * Desde el menu de inicio, buscar "Comando de Linea" o "Command Prompt" y abrir el programa que entrega la busqueda.
 * Apretar Win+R, escribir "cmd" en la ventan que aparece y apretar Enter.
Estaremos usando regularmente el comando de linea, asi que es importante que te acuerdes de como abrirlo. Una vez abierto, puedes hacerle click derecho al icono la barra de tareas y seleccionar Anclar a barra de tareas.

Con el terminal abierto, deberas ingresar el siguiente comando, aprentando Enter una vez que termines de escribirlo:

```bash
C:\Usuarios\NOMBRE_USUARIO>javac --version
javac 11.0.1
```
Como puedes observar, el comando escrito es `javac --version`. El texto inicial, `C:\Usuarios\NOMBRE_USUARIO>` indica el directorio donde estas ejecutando comandos (`NOMBRE_USUARIO` hace referencia a el usuario de tu computador). Por el momento no es de mayor importancia, pero a futuro veremos como cambiar de directorio para poder ejecutar codigo en distintas carpetas. Finalmente, una vez que apretas Enter habras notado como el terminal imprime en pantalla el resultado del comando, en este caso `javac 11.0.1`. Puede que se demore un poco en ejecutar el comando, pero ese depende principalmente el programa que se este ejecutando. Lo que acabas de realizar es ejecutar un programa (`javac`) con un argumento (`--version`), lo cual le indica al programa que debe realizar una tarea especifica. En este caso, se solicita la version actual del programa, la cual se imprime en pantalla como salida (`javac 11.0.1`).

De la misma manera, los siguientes comandos a ejecutar (con sus salidas respectivas) son los siguientes:
```bash
C:\Usuarios\NOMBRE_USUARIO>python --version
Python 3.7.1
```

```bash
C:\Usuarios\NOMBRE_USUARIO>git --version
git version 2.20.0.windows.1
```

Si todos los comandos entregan las versiones respectivas bien, entonces quedaron bien instalados. En caso de que algun programa muestre un numero de version mayor al que sale en esta guia, no te preocupes, pues el software debe haber sido actualizado con respecto a cuando se elaboro esta guia. De lo contrario, puede que necesites reiniciar (para permitir que los cambios en tu computador por las instalaciones se propagen) o reinstalar los programas. Si eso no funciona, pide ayuda!

## 5. Instalar Visual Studio Code

Visual Studio Code es el ambiente de desarrollo (IDE) oficial para programar el robot en Java y C/C++ para la temporada 2019. Este IDE entrega un editor de texto personalizable y un sistema de compilado extremadamente flexible. En caso que quieras herramientas mas potentes (lease tambien como preconfiguradas y/o especializadas), puedes optar por los IDE de Jetbrains, especificamente [IntelliJ](https://www.jetbrains.com/idea/) para Java y [PyCharm](https://www.jetbrains.com/pycharm/) para Python. Ambos programas ofrecen versiones gratuitas, llamadas "Community", pero tambien puedes optar a las versiones profesionales como estudiante en el siguiente [link](https://www.jetbrains.com/student/). Para instalar Visual Studio Code, basta con que te dirijas al siguiente [link](https://code.visualstudio.com/) y hagas click sobre el boton verde de descarga. Abre e instala el programa normalmente.

## 6. Instalar toolchain WPILib

Para poder programar el robot y pasarle codigo, es necesario tener el *toolchain* adecuado. Esto es una serie de programas que toman tu codigo y en orden lo van modificando, procesando y compilando a codigo de maquina. En este caso, el sistema de compilado a ser usado se llama Gradle y las configuraciones especificas las entrega un proyecto de la comunidad FRC llamado GradleRIO. Este proyecto ha sido adoptado como el sistema de compilacion estandar para la temporada 2019 y las instrucciones de instalacion se encuentran en [este link](https://wpilib.screenstepslive.com/s/currentCS/m/79833/l/932382-installing-vs-code). El link apunta a la version Alpha del software, asi que una vez iniciada la temporada, puede cambiar o dejar de funcionar la informacion o link. En la pagina enlazada, se muestra como instalar las WPILib tools para Visual Studio Code. Una vez instalado, sigue el siguiente tutorial para crear y compilar tu primer proyecto en WPILib

## 7. Ya terminaste con la primera guia!

Una vez que hayas terminado, por favor notifica a un mentor. De acuerdo al progreso que vayan teniendo los demas estudiantes, iremos subiendos otras guias.