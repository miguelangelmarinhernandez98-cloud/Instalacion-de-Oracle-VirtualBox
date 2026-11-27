# Guía de Instalación y Uso de MkDocs: Oracle VirtualBox

![Imagen de VirtualBox](img/portada.jpg)

## 1. Inicio

Mediante las herramientas MkDocs y GitHub Pages vamos a realizar un proyecto técnico para una empresa o clientes sobre una guía de instalación, configuración y uso de VirtualBox.
Este proyecto tiene como objetivo que cualquier persona que nunca haya utilizado esta aplicación y la vaya a usar por primera vez pueda tener los conocimientos "mínimos" para poder crear máquinas virtuales y configurarlas a sus gustos.
**Autores del proyecto:** Nicolás Romero Rubiales y Miguel Ángel Marín Hernández.

## 2. Introducción

### 2.1. ¿Qué es?

Oracle VirtualBox es una herramienta de virtualización de escritorio que permite a los usuarios ejecutar múltiples sistemas operativos en una única máquina física. Esto quiere decir que si tienes un ordenador con Windows/Linux/macOS puedes crear una máquina virtual con cualquier otro sistema operativo dentro de él para utilizarlo. Además, al ser de código abierto, es accesible y utilizado en diversas aplicaciones, desde pruebas de software hasta entornos de desarrollo.
Fue creado por la empresa alemana Innotek GmbH y actualmente es desarrollado por Oracle Corporation.

### 2.2. Características principales

VirtualBox ofrece bastante más que una ventana donde arrancar otro sistema. Entre las funciones que utilizaremos a lo largo de esta serie se encuentran:

- Snapshots para guardar puntos de estado de una VM.
- Clonado de máquinas virtuales.
- Redes NAT, bridge, host-only, internal network y NAT Network.
- Firmware BIOS y UEFI según arquitectura y configuración.
- TPM virtual en escenarios compatibles.
- Discos virtuales VDI, VMDK y otros formatos soportados.
- Controladores de almacenamiento SATA, SCSI, NVMe y otros según plataforma.
- Guest Additions para mejorar la integración con el sistema invitado.
- Passthrough de determinados dispositivos USB.
- Importación y exportación OVF/OVA.
- Administración por línea de comandos con VBoxManage.
- Modo headless para ejecutar VMs sin mantener abierta la interfaz gráfica.

## 3. Requisitos

Para una instalación correcta de VirtualBox en un ordenador necesitarás:

- **Hardware:**
  - **Procesador:** Se recomienda un procesador con soporte de virtualización por hardware. Puede ser Intel VT-x o AMD-V.
  - **Memoria RAM:** Al menos 2 GB de RAM dedicada a VirtualBox, aunque es recomendable más para un rendimiento óptimo.
- **Espacio de almacenamiento:**
  - Al menos 200 MB de espacio disponible en el disco duro para la instalación del software.
- **Sistema operativo:**
  - VirtualBox es compatible con una amplia gama de sistemas operativos, incluyendo Windows, macOS, Linux y Solaris.
- **Otros requisitos:**
  - **Acceso de administrador:** Es posible que necesites permisos de administrador en el sistema para poder instalar VirtualBox correctamente.
  - **Conexión a internet:** Para poder descargar la última versión de VirtualBox, con sus respectivas imágenes de sistemas operativos.

## 4. Instalación y uso

### 4.1. Descarga

Entramos en la página oficial de VirtualBox y nos vamos al apartado de descargas, elegimos el sistema operativo en el que queremos el ejecutable, en este caso **Windows hosts**. La página ofrece la última versión. Una vez hecho, aparece descargado el `.exe`, lo siguiente sería darle doble clic para comenzar la instalación.

![Captura 01 - Página de descarga de VirtualBox](img/cap01.png)
![Captura 02 - Ejecutable descargado](img/cap02.png)

### 4.2. Instalación

Comenzada la instalación, la primera pantalla nos da la bienvenida del asistente y nos muestra la versión de VirtualBox con la arquitectura de 64 bits, le damos a **Next** y nos lleva a la siguiente pantalla en la que nos muestra el contrato de la licencia, gran parte del código GPL, marcamos el cuadro de que aceptamos los términos y le damos a **Next**. La siguiente nos indica la selección de componentes, como VirtualBox Application, USB support, etc. Los componentes se dejan por defecto y la ruta nos indica dónde se ubica la instalación. Le damos a **Next** y en el siguiente apartado vemos un aviso que indica que la red se desconectará durante unos segundos durante la instalación, le damos a **Yes** y continuamos.
En la siguiente pantalla nos indica que, si queremos usar VirtualBox desde Python, hacen falta una serie de componentes, le damos a **Yes**. Después aparecen las opciones de inicio: añadir al menú de inicio, crear un acceso directo al escritorio y abrir los archivos OVA y OVF de VirtualBox. Se dejan marcadas como aparecen y le damos a **Next**. Ya está listo para la instalación, indicamos **Install** y se procede a instalar todo. Por último, nos muestra que la instalación ha terminado y le damos a **Finish**.

![Captura 03 - Bienvenida del asistente](img/cap03.png)
![Captura 04 - Contrato de licencia](img/cap04.png)
![Captura 05 - Selección de componentes](img/cap05.png)
![Captura 06 - Aviso de desconexión de red](img/cap06.png)
![Captura 07 - Dependencias de Python](img/cap07.png)
![Captura 08 - Opciones de inicio](img/cap08.png)
![Captura 09 - Listo para instalar](img/cap09.png)
![Captura 10 - Instalación finalizada](img/cap10.png)

### 4.3. Primer arranque

Se abre el administrador de VirtualBox, esta es la pantalla principal donde aparecerán todos los sistemas operativos que tengas.

![Captura 11 - Pantalla principal de VirtualBox](img/cap11.png)

### 4.4. Crear la máquina virtual

Para crear una máquina le damos al botón de **Nueva** y se abren las siguientes pestañas en las que tenemos que configurarlo como queramos. En la primera indicamos el nombre, la carpeta de las máquinas y, si tenemos la imagen ISO del sistema operativo, la seleccionamos. Una vez puesta la ISO, VirtualBox detecta el sistema operativo y su arquitectura. En la siguiente pestaña podemos poner el nombre y la contraseña del usuario y también indicar si queremos instalar las Guest Additions. En la siguiente indicamos cuánta memoria RAM y procesadores queremos utilizar en la máquina y, por último, cuántos GB utilizaremos en el disco duro. Una vez terminado podemos ver que se está iniciando Ubuntu junto con las características configuradas de dicha máquina.

![Captura 12 - Nombre y sistema operativo](img/cap12.png)
![Captura 13 - Instalación desatendida y usuario](img/cap13.png)
![Captura 14 - Asignación de memoria RAM y CPU](img/cap14.png)
![Captura 15 - Creación de disco duro virtual](img/cap15.png)
![Captura 16 - Resumen e inicio de la máquina](img/cap16.png)

### 4.5. Uso de la máquina

Vemos que Ubuntu se ha arrancado correctamente y podemos utilizarlo como cualquier otro sistema operativo.
Cuando apagamos la máquina aparece **Apagada** y la unidad óptica aparece vacía, ya que la ISO ya no se utiliza.

![Captura 17 - Ubuntu funcionando](img/cap17.png)
![Captura 18 - Máquina virtual apagada](img/cap18.png)

### 4.6. Configuración de la máquina virtual Ubuntu

Entramos en la configuración de Ubuntu Desktop y podemos destacar varias opciones y modificarlas. Las pestañas de **General**, **Sistema**, **Almacenamiento** y **Red** son las más destacadas, pudiendo modificar o añadir más almacenamiento o adaptadores de red en las máquinas.

![Captura 19 - Configuración General y Sistema](img/cap19.png)
![Captura 20 - Configuración de Almacenamiento](img/cap20.png)
![Captura 21 - Configuración de Red](img/cap21.png)

### 4.7. Menús principales

En la pestaña inicial, en la parte superior izquierda existen varias pestañas que sirven como menús con distintas opciones. La primera es **Archivo**, donde están las preferencias y ajustes generales, importar y/o exportar servicios virtualizados, herramientas, actualizaciones y advertencias. Después está la pestaña **Máquina**, en la que encontramos acciones como **Nueva**, para crear una máquina virtual; **Clonar**, para duplicar una máquina; **Mover** y **Eliminar**; e iniciar, pausar, reiniciar y parar las máquinas, entre muchas otras opciones.

![Captura 22 - Menú Archivo](img/cap22.png)
![Captura 23 - Menú Máquina](img/cap23.png)

## 5. Funcionamiento y beneficios

VirtualBox permite crear entornos que serían incómodos o costosos de reproducir con hardware físico. Algunos usos habituales son:

- Probar una distribución GNU/Linux sin reemplazar el sistema principal.
- Mantener laboratorios con varias versiones de Windows y Linux.
- Desarrollar y probar software en diferentes sistemas operativos.
- Montar redes virtuales para estudiar administración, routing o seguridad.
- Probar actualizaciones y configuraciones antes de aplicarlas a un equipo real.
- Crear snapshots para experimentar y regresar rápidamente a un estado anterior.
- Importar y exportar appliances en formatos OVF/OVA.
- Automatizar máquinas virtuales mediante VBoxManage.
- Ejecutar entornos temporalmente aislados del sistema principal.

La virtualización no hace que los recursos sean infinitos. Si creamos cuatro VMs y asignamos 8 GB de RAM a cada una, el host necesita disponer de memoria suficiente para sostenerlas además de ejecutar su propio sistema operativo.

### Beneficios de usar la virtualización

Ofrece una serie de beneficios significativos para individuos y organizaciones, entre los que destacan:

- **Optimización de recursos:** La virtualización permite utilizar de manera más eficiente los recursos de hardware al permitir que múltiples sistemas operativos y aplicaciones se ejecuten en un único servidor físico. Esto reduce la necesidad de tener múltiples servidores físicos, lo que ahorra espacio, energía y costos de mantenimiento.
- **Flexibilidad y escalabilidad:** La virtualización permite crear y desplegar rápidamente nuevas máquinas virtuales según sea necesario, lo que facilita la adaptación a cambios en la demanda de recursos informáticos. Esto permite a las organizaciones escalar sus recursos de TI de manera más eficiente para satisfacer las necesidades del negocio.
- **Facilita el desarrollo y la prueba:** La virtualización proporciona un entorno aislado y seguro para el desarrollo y la prueba de software. Los desarrolladores pueden crear fácilmente entornos de desarrollo reproducibles y los probadores pueden probar aplicaciones en diferentes configuraciones de sistemas operativos sin afectar el entorno de producción.
- **Recuperación ante desastres y alta disponibilidad:** Mediante la virtualización, es posible realizar copias de seguridad completas de las máquinas virtuales, lo que facilita la recuperación ante desastres y la continuidad del negocio en caso de fallo del hardware o de otros eventos catastróficos. Además, la migración en caliente y otras tecnologías de alta disponibilidad permiten mantener las aplicaciones en funcionamiento incluso durante el mantenimiento del hardware o la actualización del software.
- **Consolidación del centro de datos:** La virtualización permite consolidar múltiples servidores físicos en un único servidor físico o en un conjunto de servidores físicos. Esto puede reducir significativamente la cantidad de hardware necesario en un centro de datos, lo que a su vez reduce los costos de adquisición, energía y refrigeración, así como simplifica la gestión y el mantenimiento del entorno de TI.

## 6. Conclusiones y aprendizajes

En resumen, VirtualBox es una herramienta muy sencilla y fácil de usar para tener y utilizar varios sistemas operativos en un mismo ordenador. Permite probar configuraciones de software en un entorno aislado y con opciones de volver atrás con las instantáneas. Es muy recomendable para el aprendizaje sobre sistemas operativos y administración de dichos sistemas ya que no hay riesgo en el ordenador principal.

- Distinguir entre el equipo anfitrión y el invitado.
- Reservar bien los recursos para evitar problemas de rendimiento.
- Hacer instantáneas para experimentar sin miedo y volver atrás cuando quieras.
- Instalar las Guest Additions para tener más funciones y tener una máquina cómoda de usar.

### Bibliografía y enlaces de interés

- [Universo Digital - Características de VirtualBox](https://universodigital.org/caracteristicas-de-virtualbox-introduccion/)
- [Xataka Basics - VirtualBox: qué es y cómo usarlo](https://www.xataka.com/basics/virtualbox-que-como-usarlo-para-crear-maquina-virtual-windows-u-otro-sistema-operativo)
- [Introducción al software de virtualización Oracle VirtualBox](https://antoniovf.wordpress.com/2012/07/13/introduccion-al-software-de-virtualizacion-oracle-virtualbox/)
- [Studocu - Introducción a VirtualBox](https://www.studocu.com/co/document/universidad-autonoma-del-caribe/el-rol-de-docente-universitario-del-siglo-xxi/introduccion-a-virtual-box/99286694?sid=e7bb2ac3-b678-4252-a59f-1ee374b7c5a71795544023)
- [Prezi - Introducción a VirtualBox](https://prezi.com/p/brx3ugkljixa/introduccion-a-virtualbox/)
- [Studocu - Instalación de VirtualBox](https://www.studocu.com/es-mx/document/instituto-tecnologico-superior-de-alvarado/programacion-de-base-de-datos/instalalcion-de-virtualbox-)
- [AOMEI Tech - Crear máquina virtual con VirtualBox](