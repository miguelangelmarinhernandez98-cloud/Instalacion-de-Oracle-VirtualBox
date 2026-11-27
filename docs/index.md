<center><h2 id="guia-virtualbox"><strong>Gu├¡a de Instalaci├│n y Uso de MkDocs: Oracle VirtualBox</strong></h2></center>

<center><img src="img/portada.jpg" alt="Imagen de VirtualBox" class="img-fluid"></center>

<p id="inicio"><strong>1. Inicio.</strong></p>
<p>Mediante las herramientas MkDocs y GitHub Pages vamos a realizar un proyecto t├®cnico para una empresa o clientes sobre una gu├¡a de instalaci├│n, configuraci├│n y uso de VirtualBox.</p>
<p>Este proyecto tiene como objetivo que cualquier persona que nunca haya utilizado esta aplicaci├│n y la vaya a usar por primera vez pueda tener los conocimientos ÔÇ£m├¡nimosÔÇØ para poder crear m├íquinas virtuales y configurarlas a sus gustos.</p>
<p>Autores del proyecto: Nicol├ís Romero Rubiales y Miguel ├üngel Mar├¡n Hern├índez.</p>

<p id="introduccion"><strong>2. Introducci├│n.</strong></p>
<p><strong>2.1. ┬┐Qu├® es?</strong></p>
<p>Oracle VirtualBox es una herramienta de virtualizaci├│n de escritorio que permite a los usuarios ejecutar m├║ltiples sistemas operativos en una ├║nica m├íquina f├¡sica. Esto quiere decir que si tienes un ordenador con Windows/Linux/macOS puedes crear una m├íquina virtual con cualquier otro sistema operativo dentro de ├®l para utilizarlo. Adem├ís, al ser de c├│digo abierto, es accesible y utilizado en diversas aplicaciones, desde pruebas de software hasta entornos de desarrollo.</p>
<p>Fue creado por la empresa alemana Innotek GmbH y actualmente es desarrollado por Oracle Corporation.</p>

<p id="caracteristicas"><strong>2.2. Caracter├¡sticas principales.</strong></p>
<p>VirtualBox ofrece bastante m├ís que una ventana donde arrancar otro sistema. Entre las funciones que utilizaremos a lo largo de esta serie se encuentran:</p>
<p>┬À Snapshots para guardar puntos de estado de una VM.</p>
<p>┬À Clonado de m├íquinas virtuales.</p>
<p>┬À Redes NAT, bridge, host-only, internal network y NAT Network.</p>
<p>┬À Firmware BIOS y UEFI seg├║n arquitectura y configuraci├│n.</p>
<p>┬À TPM virtual en escenarios compatibles.</p>
<p>┬À Discos virtuales VDI, VMDK y otros formatos soportados.</p>
<p>┬À Controladores de almacenamiento SATA, SCSI, NVMe y otros seg├║n plataforma.</p>
<p>┬À Guest Additions para mejorar la integraci├│n con el sistema invitado.</p>
<p>┬À Passthrough de determinados dispositivos USB.</p>
<p>┬À Importaci├│n y exportaci├│n OVF/OVA.</p>
<p>┬À Administraci├│n por l├¡nea de comandos con VBoxManage.</p>
<p>┬À Modo headless para ejecutar VMs sin mantener abierta la interfaz gr├ífica.</p>

<p id="requisitos"><strong>3. Requisitos.</strong></p>
<p>Para una instalaci├│n correcta de VirtualBox en un ordenador necesitar├ís:</p>
<p><strong>Hardware:</strong></p>
<p>Procesador: Se recomienda un procesador con soporte de virtualizaci├│n por hardware. Puede ser Intel VT-x o AMD-V.</p>
<p>Memoria RAM: Al menos 2GB de RAM dedicada a VirtualBox, aunque es recomendable m├ís para un rendimiento ├│ptimo.</p>
<p><strong>Espacio de almacenamiento:</strong></p>
<p>Al menos 200MB de espacio disponible en el disco duro para la instalaci├│n del software.</p>
<p><strong>Sistema operativo:</strong></p>
<p>Virtualbox es compatible con una amplia gama de sistemas operativos, incluyendo Windows, macOS, Linux y Solaris.</p>
<p><strong>Otros requisitos:</strong></p>
<p>Acceso de administrador: Es posible que necesites permisos de administrador en el sistema para poder instalar VirtualBox correctamente.</p>
<p>Conexi├│n a internet: Para poder descargar la ├║ltima versi├│n de VirtualBox, con sus respectivas im├ígenes de sistemas operativos.</p>

<p id="instalacion-uso"><strong>4. Instalaci├│n y uso.</strong></p>

<p id="descarga"><strong>4.1. Descarga. (capturas 01 y 02)</strong></p>
<p>Entramos en la p├ígina oficial de VirtualBox y nos vamos al apartado de descargas, elegimos el sistema operativo en el que queremos el ejecutable, en este caso Windows hosts. La p├ígina ofrece la ├║ltima versi├│n. Una vez hecho, aparece descargado el .exe, lo siguiente ser├¡a darle doble clic para comenzar la instalaci├│n.</p>
<div class="my-3 text-center">
    <img src="img/cap01.png" alt="Captura 01 - P├ígina de descarga de VirtualBox" class="img-fluid mb-3 border rounded shadow-sm">
    <img src="img/cap02.png" alt="Captura 02 - Ejecutable descargado" class="img-fluid mb-3 border rounded shadow-sm">
</div>

<p id="instalacion"><strong>4.2. Instalaci├│n. (capturas 03 - 10)</strong></p>
<p>Comenzada la instalaci├│n, la primera pantalla nos da la bienvenida del asistente y nos muestra la versi├│n de VirtualBox con la arquitectura de 64 bits, le damos a ÔÇ£NextÔÇØ y nos lleva a la siguiente pantalla en la que nos muestra el contrato de la licencia, gran parte del c├│digo GPL, marcamos el cuadro de que aceptamos los t├®rminos y le damos a ÔÇ£NextÔÇØ. La siguiente nos indica la selecci├│n de componentes, como VirtualBox Application, USB support, etc. Los componentes se dejan por defecto y la ruta nos indica d├│nde se ubica la instalaci├│n. Le damos a ÔÇ£NextÔÇØ y en el siguiente apartado vemos un aviso que indica que la red se desconectar├í durante unos segundos durante la instalaci├│n, le damos a ÔÇ£YesÔÇØ y continuamos. En la siguiente pantalla nos indica que, si queremos usar VirtualBox desde Python, hacen falta una serie de componentes, le damos a ÔÇ£YesÔÇØ. Despu├®s aparecen las opciones de inicio: a├▒adir al men├║ de inicio, crear un acceso directo al escritorio y abrir los archivos OVA y OVF de VirtualBox. Se dejan marcadas como aparecen y le damos a ÔÇ£NextÔÇØ. Ya est├í listo para la instalaci├│n, indicamos ÔÇ£InstallÔÇØ y se procede a instalar todo. Por ├║ltimo, nos muestra que la instalaci├│n ha terminado y le damos a ÔÇ£FinishÔÇØ.</p>
<div class="my-3 text-center">
    <img src="img/cap03.png" alt="Captura 03 - Bienvenida del asistente" class="img-fluid mb-3 border rounded shadow-sm">
    <img src="img/cap04.png" alt="Captura 04 - Contrato de licencia" class="img-fluid mb-3 border rounded shadow-sm">
    <img src="img/cap05.png" alt="Captura 05 - Selecci├│n de componentes" class="img-fluid mb-3 border rounded shadow-sm">
    <img src="img/cap06.png" alt="Captura 06 - Aviso de desconexi├│n de red" class="img-fluid mb-3 border rounded shadow-sm">
    <img src="img/cap07.png" alt="Captura 07 - Dependencias de Python" class="img-fluid mb-3 border rounded shadow-sm">
    <img src="img/cap08.png" alt="Captura 08 - Opciones de inicio" class="img-fluid mb-3 border rounded shadow-sm">
    <img src="img/cap09.png" alt="Captura 09 - Listo para instalar" class="img-fluid mb-3 border rounded shadow-sm">
    <img src="img/cap10.png" alt="Captura 10 - Instalaci├│n finalizada" class="img-fluid mb-3 border rounded shadow-sm">
</div>

<p id="primer-arranque"><strong>4.3. Primer arranque. (captura 11)</strong></p>
<p>Se abre el administrador de VirtualBox, esta es la pantalla principal donde aparecer├ín todos los sistemas operativos que tengas.</p>
<div class="my-3 text-center">
    <img src="img/cap11.png" alt="Captura 11 - Pantalla principal de VirtualBox" class="img-fluid mb-3 border rounded shadow-sm">
</div>

<p id="crear-vm"><strong>4.4. Crear la m├íquina virtual. (capturas 12-16)</strong></p>
<p>Para crear una m├íquina le damos al bot├│n de ÔÇ£NuevaÔÇØ y se abren las siguientes pesta├▒as en las que tenemos que configurarlo como queramos. En la primera indicamos el nombre, la carpeta de las m├íquinas y, si tenemos la imagen ISO del sistema operativo, la seleccionamos. Una vez puesta la ISO, VirtualBox detecta el sistema operativo y su arquitectura. En la siguiente pesta├▒a podemos poner el nombre y la contrase├▒a del usuario y tambi├®n indicar si queremos instalar las Guest Additions. En la siguiente indicamos cu├ínta memoria RAM y procesadores queremos utilizar en la m├íquina y, por ├║ltimo, cu├íntos GB utilizaremos en el disco duro. Una vez terminado podemos ver que se est├í iniciando Ubuntu junto con las caracter├¡sticas configuradas de dicha m├íquina.</p>
<div class="my-3 text-center">
    <img src="img/cap12.png" alt="Captura 12 - Nombre y sistema operativo" class="img-fluid mb-3 border rounded shadow-sm">
    <img src="img/cap13.png" alt="Captura 13 - Instalaci├│n desatendida y usuario" class="img-fluid mb-3 border rounded shadow-sm">

    <img src="img/cap14.png" alt="Captura 14 - Asignaci├│n de memoria RAM y CPU" class="img-fluid mb-3 border rounded shadow-sm">
    <img src="img/cap15.png" alt="Captura 15 - Creaci├│n de disco duro virtual" class="img-fluid mb-3 border rounded shadow-sm">
    <img src="img/cap16.png" alt="Captura 16 - Resumen e inicio de la m├íquina" class="img-fluid mb-3 border rounded shadow-sm">
</div>

<p id="uso-vm"><strong>4.5. Uso de la m├íquina. (capturas 17-18)</strong></p>
<p>Vemos que Ubuntu se ha arrancado correctamente y podemos utilizarlo como cualquier otro sistema operativo.</p>
<p>Cuando apagamos la m├íquina aparece ÔÇ£ApagadaÔÇØ y la unidad ├│ptica aparece vac├¡a, ya que la ISO ya no se utiliza.</p>
<div class="my-3 text-center">
    <img src="img/cap17.png" alt="Captura 17 - Ubuntu funcionando" class="img-fluid mb-3 border rounded shadow-sm">
    <img src="img/cap18.png" alt="Captura 18 - M├íquina virtual apagada" class="img-fluid mb-3 border rounded shadow-sm">
</div>

<p id="configuracion-vm"><strong>4.6. Configuraci├│n de la m├íquina virtual Ubuntu. (capturas 19-21)</strong></p>
<p>Entramos en la configuraci├│n de Ubuntu Desktop y podemos destacar varias opciones y modificarlas. Las pesta├▒as de General, Sistema, Almacenamiento y Red son las m├ís destacadas, pudiendo modificar o a├▒adir m├ís almacenamiento o adaptadores de red en las m├íquinas.</p>
<div class="my-3 text-center">
    <img src="img/cap19.png" alt="Captura 19 - Configuraci├│n General y Sistema" class="img-fluid mb-3 border rounded shadow-sm">
    <img src="img/cap20.png" alt="Captura 20 - Configuraci├│n de Almacenamiento" class="img-fluid mb-3 border rounded shadow-sm">
    <img src="img/cap21.png" alt="Captura 21 - Configuraci├│n de Red" class="img-fluid mb-3 border rounded shadow-sm">
</div>

<p id="menus-principales"><strong>4.7. Men├║s principales. (capturas 22-23)</strong></p>
<p>En la pesta├▒a inicial, en la parte superior izquierda existen varias pesta├▒as que sirven como men├║s con distintas opciones. La primera es ÔÇ£ArchivoÔÇØ, donde est├ín las preferencias y ajustes generales, importar y/o exportar servicios virtualizados, herramientas, actualizaciones y advertencias. Despu├®s est├í la pesta├▒a ÔÇ£M├íquinaÔÇØ, en la que encontramos acciones como Nueva, para crear una m├íquina virtual; Clonar, para duplicar una m├íquina; Mover y Eliminar; y iniciar, pausar, reiniciar y parar las m├íquinas, entre muchas otras opciones.</p>
<div class="my-3 text-center">
    <img src="img/cap22.png" alt="Captura 22 - Men├║ Archivo" class="img-fluid mb-3 border rounded shadow-sm">
    <img src="img/cap23.png" alt="Captura 23 - Men├║ M├íquina" class="img-fluid mb-3 border rounded shadow-sm">
