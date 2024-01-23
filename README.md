<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
</head>
<body>
     <h1>LightScribe en Linux</h1>
    <p>LightScribe es una innovadora tecnología que posibilita la impresión de etiquetas directamente en discos CD/DVD compatibles. A pesar de que HP cesó oficialmente el soporte de LightScribe en diciembre de 2013,​ la comunidad ha continuado manteniendo esta tecnología de manera independiente.</p>
    <p>En un esfuerzo por preservar y compartir la utilidad de LightScribe, he recopilado y subido los archivos de instalación de LaCie y LightScribe a mi repositorio personal. Esta iniciativa permite a los usuarios acceder a estos recursos y disfrutar de las capacidades de LightScribe en sistemas Linux.</p>
    <h2>Archivos disponibles</h2>
    <pre>
usuario@usuario:/media/usuario/LightScribe$ ls -l
total 13668
-rw-rw-r-- 1 usuario usuario  3119250 ago  2  2015 4l_1.0-1_i386.deb
-rw-rw-r-- 1 usuario usuario   823350 ene 22 02:32 lightscribe-1.18.27.10-linux-2.6-intel.deb
-rw-rw-r-- 1 usuario usuario 10044672 ene 22 02:32 lightscribeApplications-1.18.15.1-linux-2.6-intel.deb
usuario@usuario:/media/usuario/LightScribe$ 
    </pre>
    <p>Estos son los archivos disponibles para LightScribe en Linux. Puedes descargar e instalar estos paquetes Debian (<code>.deb</code>) en tu sistema.</p>
    <h2>Instalación</h2>
    <h3>Instalación en 32-Bit</h3>
    <p>Si utilizás un sistema 32 bit, abrí un terminal y escribí los siguientes comandos:</p>
    <pre>
sudo dpkg -i lightscribe*.deb
sudo dpkg -i 4l*.deb
    </pre>
    <h3>Instalación en 64-Bit</h3>
    <p>Si utilizás un sistema 64 bit, será necesario forzar la instalación. Antes, conviene siempre hacer un backup del sistema. Los comandos a ejecutar para realizar la instalación son los siguientes:</p>
    <pre>
sudo dpkg --install --force architecture lightscribe*.deb
sudo dpkg --install --force-architecture 4l*.deb
    </pre>
    <p><strong>Burn, baby, burn</strong></p>
    <p>Para crear un disco con una imagen, ejecutá 4L-gui con privilegios de administrador:</p>
    <pre>
sudo 4L-gui
    </pre>
    <p>En caso de que sólo necesites imprimir un texto breve, ejecutá SimpleLabeler así:</p>
    <pre>
/opt/lightscribeApplications/SimpleLabeler/SimpleLabeler
    </pre>
    <p>Para habilitar un alto contraste en la imagen impresa:</p>
    <pre>
sudo /usr/lib/lightscribe/elcu.sh
    </pre>
    <p>El proceso de quemado de los discos utilizando LightScribe puede tardar un buen rato.</p>
</body>
</html>

