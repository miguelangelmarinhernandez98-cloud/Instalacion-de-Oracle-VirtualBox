Memoria Técnica del Proyecto: Guía de Instalación y Uso de Oracle VirtualBox con MkDocs y GitHub Pages

Autores: Nicolás Romero Rubiales y Miguel Ángel Marín Hernández
Repositorio GitHub: https://github.com/miguelangelmarinhernandez98-cloud/Instalacion-de-Oracle-VirtualBox
Sitio web publicado: https://miguelangelmarinhernandez98-cloud.github.io/Instalacion-de-Oracle-VirtualBox/

Objetivo y arquitectura del proyecto

El objetivo de este proyecto ha sido migrar y transformar una guía técnica sobre la instalación, configuración y uso de Oracle VirtualBox en un portal de documentación web moderno, estructurado y accesible públicamente mediante MkDocs y GitHub Pages.

Estructura del repositorio y gestión de ramas:
El repositorio se ha organizado siguiendo buenas prácticas de control de versiones con Git. La rama main contiene el código fuente del proyecto (mkdocs.yml), los archivos Markdown (docs/), los recursos gráficos (docs/img/) y las plantillas sobrescritas (overrides/). La rama gh-pages está dedicada exclusivamente al despliegue del sitio estático compilado, generada automáticamente mediante el comando mkdocs gh-deploy. Asimismo, mediante el archivo .gitignore se ha excluido la carpeta temporal de compilación (site/) del seguimiento en main para evitar duplicidades y mantener limpio el historial de commits.

Configuración de MkDocs y Tema Utilizado (mkdocs.yml)

Para ofrecer una interfaz limpia, minimalista y adaptada a documentación técnica moderna, se ha utilizado el tema shadcn (mkdocs-shadcn), configurado en el archivo raíz mkdocs.yml. En él se han definido los metadatos del sitio mediante site_name ("Guía de instalación y uso de Oracle VirtualBox"), site_description y site_author. También se han ajustado las opciones del tema: show_title en true para mostrar el título principal en la cabecera superior, show_stargazers en false para ocultar el contador de estrellas de GitHub y mantener una interfaz centrada en la lectura, y custom_dir apuntando a overrides para habilitar la personalización de plantillas HTML del tema sin modificar los archivos originales del paquete Python.

Personalización de Interfaz (overrides/)

Dado que el tema shadcn presenta por defecto sus elementos de interfaz en inglés, se ha sobrescrito su plantilla HTML dentro del directorio overrides/ para localizar el sitio completo al español, traduciendo el índice lateral de contenidos de "On This Page" a "En esta página" y el cuadro de búsqueda integrado de "Search documentation..." a "Buscar en la guía...".

Bloques y Estructura del Contenido (docs/index.md)

La documentación se ha redactado íntegramente en Markdown con codificación UTF-8, utilizando jerarquía de encabezados para generar automáticamente la tabla de contenidos interactiva, listas, énfasis y bloques de código en línea para comandos y extensiones.

El contenido se divide en seis bloques principales. El primero, Inicio, presenta el proyecto técnico, los objetivos de aprendizaje y la autoría. El segundo, Introducción, define Oracle VirtualBox como hipervisor de escritorio y detalla sus características principales como snapshots, clonado, modos de red NAT, Bridge y Host-Only, firmware BIOS y UEFI, TPM virtual, formatos VDI y VMDK, Guest Additions, VBoxManage y modo headless. El tercero, Requisitos, recoge las especificaciones mínimas y recomendadas de hardware (virtualización asistida Intel VT-x o AMD-V y memoria RAM), almacenamiento, sistemas operativos anfitriones compatibles y permisos necesarios. El cuarto, Instalación y uso, ofrece una guía paso a paso ilustrada con 24 recursos gráficos (portada.jpg y de cap01.png a cap23.png almacenados en docs/img/), cubriendo desde la descarga del instalador en Windows hasta el asistente de instalación, el primer arranque, la creación de una máquina virtual Ubuntu, su uso básico, la configuración de hardware y red y la exploración de los menús principales Archivo y Máquina. El quinto, Funcionamiento y beneficios, expone los casos de uso habituales en entornos de desarrollo y administración de sistemas, la gestión de recursos del equipo anfitrión y las ventajas clave de la virtualización como optimización, escalabilidad, aislamiento, recuperación ante desastres y consolidación. Por último, el sexto bloque, Conclusiones, aprendizajes y bibliografía, sintetiza las buenas prácticas recomendadas al trabajar con máquinas virtuales e incluye los enlaces de referencia consultados.
