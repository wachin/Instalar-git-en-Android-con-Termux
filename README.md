# Instalar-git-en-Android-con-Termux
Como Instalar git en Android con Termux para usar Github como almacenamiento en la nube 

Aquí tienes el texto convertido a Markdown:

---

### Termux: Emulador de Terminal y Entorno Linux en Android

Termux es como un emulador de terminal y entorno Linux, y gracias a él, en Android podemos instalar Git para usarlo como lo haríamos desde una terminal de Linux. Además, podemos instalar otros programas como:

- **yt-dlp** (para descargar videos de YouTube)
- **nnn** (Administrador de Archivos)
- y otros, siempre que se puedan usar desde la terminal.

### El Porqué de Este Tutorial

En MX Linux 21 estoy usando Git como un tipo de almacenamiento en la nube, similar a:

- Dropbox
- MEGA
- Google Drive

Lo mismo hago con Git desde mi celular Android en Termux para tener mis archivos offline.

Ejemplo: He creado un cancionero con acordes de guitarra para usarlo tanto en mi celular Android como en mi ordenador con Linux:

[https://github.com/wachin/Cancionero](https://github.com/wachin/Cancionero)

> **Nota:** Con la App de GitHub de Microsoft disponible en la Play Store no se puede hacer todo lo que se puede hacer con Git desde la terminal de Termux.

### Pros

- Archivos offline en el celular.

### Cosas a Saber

- Sincronización manual.
- Un repositorio de Git contiene una copia de sus archivos en la carpeta oculta `.git`, lo que puede ocupar el doble de espacio o más.
- Usuarios avanzados con conocimientos en control de versiones con Git.
- Usar la terminal.

### Requerimientos

- Teléfono con Android.
- Repositorio en [GitHub](https://github.com).

### Archivos Usables

Se pueden usar archivos para control de versiones como `.txt`, `.md`, u otros. En los archivos compatibles con control de versiones solo se aumentará el tamaño del archivo donde se edite y agregue información.

> **Nota:** LibreOffice tiene un archivo para control de versiones: `.fodt`. Más información en: [Qué es un archivo FODT](https://facilitarelsoftwarelibre.blogspot.com/2020/06/que-es-un-archivo-fodt-fodt-flat-open.html), pero no hay un editor para este tipo de archivo en la Play Store.

Si un archivo no es compatible con control de versiones, después de hacer `push`, si lo vuelve a editar, se copiará dos veces, y así sucesivamente, lo que ocupará más espacio.

Yo además uso `.docx`, un tipo de archivo que utilizo en WPS Office (similar al de Microsoft Office), que no es compatible con control de versiones. Sin embargo, lo uso para escribir acordes de guitarra, que no suelen ocupar mucho espacio.

### ¿Qué Más se Puede Hacer con Git?

- Se puede hacer `push`, `fetch`, `merge`, y todos los demás comandos para mantener sincronizado el repositorio.
- Se puede trabajar con los archivos desde:

  - Android a Linux y viceversa.
  - Android a Windows y viceversa.
  - Android a Mac y viceversa.

> **Nota:** Los dos últimos no los he probado, pero sé que existen.

### Compatibilidad Entre Android y Linux

En el siguiente video:

[Aprende GIT Ahora! Curso completo gratis desde cero](https://youtu.be/VdGzPZ31ts8)

Allí, Nicolás Schurmann explica que si se sincroniza un repositorio desde Windows a "Linux o Mac", deben configurar el fin de línea para enviar ediciones en código de texto. Pero en este tutorial no es necesario, ya que usar Git desde Termux es como usarlo en Linux, y luego lo uso en mi ordenador con Linux, por lo que no hace falta hacer esta configuración adicional.

Este tutorial no pretende enseñarle a usar Git. Si no sabe, puede buscar en Google las palabras "aprende Git cursos" y encontrará opciones en:

- Udemy
- Platzi
- Devcode
- EDteam
- Coursera
- [GitHub](https://github.com/JJ/aprende-git)
- YouTube, etc.

Es necesario que lo sepa usar bien, porque llega un momento en que, al editar un mismo archivo desde dispositivos diferentes (en este caso, desde un celular y un ordenador), se crean diferencias y hay que hacer `merge`.

### Instalando Termux y Git en Android 7, 8, 9, 10, 11, 12, 13, 14+

Le dejo dos opciones:

#### 1ra Opción: Instalación con Xiaomi

Si usted tiene un celular Xiaomi, busque en la tienda de aplicaciones:

- **Mi Picks**
- **GetApps**

y busque **Termux**. Instálelo y ábralo.

#### Actualizar y Automáticamente Buscar un Repositorio y Actualizar

Si solo va a usar Git en Termux, siga los siguientes pasos:

```bash
pkg update
```

Aparecerá un mensaje que dice:

"Testing the available mirrors:"

Esto significa:

"Probando los espejos disponibles:"

Esto buscará un repositorio activo.

También aparece un mensaje:

"Calculating upgrade... Done.
The following NEW packages will be installed:"

=

"Calculando actualización... Listo.
Se instalarán los siguientes paquetes NUEVOS:"

> **Explicación:** Si usted es usuario de Linux, sabrá que primero hay que poner `update` y luego `upgrade`, pero aquí ya no es necesario; `update` es como un híbrido.

Le preguntará:

`Do you want to continue? [Y/n]`

Ponga:

`y` y presione ENTER.

Esté atento, porque luego le volverá a preguntar; hay que poner como 5 veces `y`.

Ahora sí, instale Git con:

```bash
pkg install git
```

y se instalará sin más.

> **Nota:** `update` hay que hacerlo con alguna frecuencia, puede ser cada mes o cada dos meses. Es para mantener Git actualizado, ya que de lo contrario puede que en algún momento no funcione y le dé algún error inesperado al clonar algún repositorio, por ejemplo:

```bash
Receiving objects:  82% (620/754), 19.02 MiB |error: RPC failed; curl 56 OpenSSL SSL_read: Connection reset by peer, errno 104
error: 666 bytes of body are still expected
fetch-pack: unexpected disconnect
```

Para que Termux tenga acceso a su almacenamiento interno, ponga:

```bash
termux-setup-storage
```

y presione Enter y acepte.

#### 2da Opción: F-Droid

Si tiene, por ejemplo, un Samsung, según leí en:

[Termux en GitHub](https://github.com/termux/termux-app)

La versión de Termux en la Play Store está obsoleta, y la solución es ir a:

[F-Droid](https://f-droid.org/)

F-Droid es un repositorio de aplicaciones de software libre para dispositivos Android. Funciona como una alternativa a Google Play Store, proporcionando aplicaciones que son de código abierto y, en muchos casos, centradas en la privacidad. Los usuarios pueden descargar la aplicación F-Droid y, a través de ella, acceder a una variedad de aplicaciones que cumplen con estos criterios. F-Droid se distingue por su compromiso con la transparencia y la ética en el desarrollo de software, promoviendo la distribución de aplicaciones sin rastreadores ni anuncios invasivos.

Descargue e instale F-Droid; para eso le pedirá (omita este paso si ya lo ha hecho) activar en su celular la opción para instalar programas desde fuentes externas. Luego, ábralo y espere a que se actualicen los repositorios en F-Droid (unos minutos). Luego, busque dándole clic en la lupa que está a la derecha abajo:

"Termux Emulador de terminal con paquetes"

e instálelo (le pedirá una confirmación especial de que acepta la instalación de una fuente externa).

Si tiene alguna duda, suba el archivo a:

[www.virustotal.com](https://www.virustotal.com)

> **Nota:** También se puede instalar directamente Termux APK desde (sin instalar F-Droid):

[Termux en F-Droid](https://f-droid.org/en/packages/com.termux/)

Descárguelo e instálelo.

O también se puede instalar desde GitHub (descargue el Universal):

[Termux en GitHub](https://github.com/termux/termux-app/releases)

Después de instalar Termux, ábralo. Le pedirá que permita acceder a sus archivos; acepte y luego escriba:

```bash
pkg update
```

y luego escriba:

```bash
pkg install git
```

Espere a que se instale. Si todo sale bien, le preguntará en inglés y ponga "y". Pero suponiendo que no se pueda a la primera vez (le puede salir algún mensaje de error), inténtelo otra vez y debería poderse. Luego ponga:

```bash
termux-setup-storage
```

Para ver la versión que tiene instalada de Git, ponga en Termux:

```bash
git --version
```

> **Nota:** Si desea instalar `yt-dlp` para descargar videos de YouTube, en mi experiencia personal de 2 años usando Termux, debe elegir un repositorio manualmente y tener 2 o 3 opciones que sean compatibles. Esto es porque al instalar Python, hay unas librerías que un repositorio puede tener más actualizadas que otro y no funcionar la instalación de `yt-dlp`. Para eso, haré luego un tutorial.

---

### Zoom en Termux

Si la letra de Termux es muy pequeña
