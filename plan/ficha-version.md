
# Ficha de verificación de versiones - Grupo 09

**Universidad:** Universidad del Valle - Sede Yumbo  
**Asignatura:** Sistemas Operativos (2026-2)  
**Integrante:** Jaider Stiven Valencia Orobio  
**Grupo:** 09  
**Fecha de consulta:** 19 de noviembre de 2026

## 1. Manjaro - Linux gráfico

**Versión elegida:** Manjaro 26.1.3 XFCE  
**Máquina virtual:** g09-grafica

| **Pregunta** | **Respuesta investigada** | **Fuente** |
| ------------ | ------------------------- | ---------- |
| 1. Versión y fecha de lanzamiento | Manjaro 26.1.3 XFCE, de la serie Bian-May. La imagen fue publicada el 28 de octubre de 2026. | [Lanzamientos oficiales de Manjaro](https://forum.manjaro.org/t/manjaro-26-1-bian-may-released/189526) |
| 2. ¿Hasta cuándo recibe actualizaciones de seguridad? | Manjaro utiliza un modelo de actualizaciones continuas (rolling release), por lo que no tiene una fecha fija de finalización del soporte por versión. Es necesario mantener el sistema actualizado. | [Modelo de actualizaciones de Manjaro](https://wiki.manjaro.org/index.php?title=The_Rolling_Release_Development_Model) |
| 3. ¿Qué hardware requiere y funciona en VirtualBox? | Utiliza arquitectura de 64 bits (x86_64) y es compatible con VirtualBox. Para este proyecto se propone asignar 2 procesadores virtuales, 4 GB de RAM y 35 GB de disco virtual. Estos valores son una configuración de laboratorio, no requisitos mínimos oficiales. | [Instalación de Manjaro](https://wiki.manjaro.org/index.php?title=Installation_Guides) |
| 4. ¿Permite el particionado manual? | Sí. Manjaro permite configurar manualmente las particiones durante la instalación. Para el proyecto se utilizarán las particiones raíz (/), swap y /home. | [Particionado en Manjaro](https://wiki.manjaro.org/index.php?title=Partitioning_Overview_and_Existing_Partition_Tables) |
| 5. ¿Existe guía oficial para Docker Engine en esta familia? | Docker no ofrece una guía oficial específica para instalar Docker Engine en Manjaro. Existen procedimientos comunitarios, pero esta distribución no aparece entre las plataformas con instrucciones oficiales específicas de Docker Engine. | [Documentación de Docker Engine](https://docs.docker.com/engine/install/) |
| 6. ¿Existe imagen base de Docker Hub para esa versión? | No se identificó una imagen oficial de Docker Hub para Manjaro 26.1.3. Existen imágenes de terceros, pero en este proyecto se utilizará Fedora como imagen base del Dockerfile. | [Docker Hub](https://hub.docker.com/search?q=manjaro&type=image) |

## 2. Ubuntu Server - Linux consola

**Versión elegida:** Ubuntu Server 26.04.1 LTS  
**Máquina virtual:** g09-consola

| **Pregunta** | **Respuesta investigada** | **Fuente** |
| ------------ | ------------------------- | ---------- |
| 1. Versión y fecha de lanzamiento | Ubuntu Server 26.04.1 LTS, Resolute Raccoon. Ubuntu 26.04 LTS fue lanzado el 23 de abril de 2026 y su actualización 26.04.1 el 27 de agosto de 2026. | [Versiones oficiales de Ubuntu](https://wiki.ubuntu.com/Releases) |
| 2. ¿Hasta cuándo recibe actualizaciones de seguridad? | Ubuntu Server 26.04 LTS cuenta con cinco años de mantenimiento estándar y recibe actualizaciones de seguridad hasta 2031. | [Notas oficiales de Ubuntu 26.04](https://documentation.ubuntu.com/release-notes/26.04/) |
| 3. ¿Qué hardware requiere y funciona en VirtualBox? | Para Ubuntu Server 26.04 LTS se indican requisitos desde 1,5 GB de RAM y 5 GB de almacenamiento. Es compatible con entornos virtualizados como VirtualBox. Para el proyecto se propone utilizar 2 procesadores virtuales, entre 2 y 4 GB de RAM y 35 GB de disco virtual. | [Descarga y requisitos de Ubuntu Server](https://ubuntu.com/download/server) |
| 4. ¿Permite el particionado manual? | Sí. Ubuntu Server utiliza el instalador Subiquity, que permite configurar manualmente las particiones mediante las opciones de almacenamiento personalizado. | [Documentación de Subiquity](https://canonical-subiquity.readthedocs-hosted.com/en/latest/howto/configure-storage.html) |
| 5. ¿Existe guía oficial para Docker Engine en esta familia? | Sí. Docker proporciona una guía oficial para instalar Docker Engine en Ubuntu, incluyendo Ubuntu 26.04 LTS. | [Instalación de Docker Engine en Ubuntu](https://docs.docker.com/engine/install/ubuntu/) |
| 6. ¿Existe imagen base de Docker Hub para esa versión? | Sí. Docker Hub dispone de la imagen oficial ubuntu:26.04. Sin embargo, esta no será la imagen base del Dockerfile del grupo 09 porque se asignó Fedora. | [Imagen oficial de Ubuntu en Docker Hub](https://hub.docker.com/_/ubuntu) |

## 3. Fedora - Imagen base del Dockerfile

**Versión elegida:** Fedora Linux 45  
**Imagen base:** fedora:45

| **Pregunta** | **Respuesta investigada** | **Fuente** |
| ------------ | ------------------------- | ---------- |
| 1. Versión y fecha de lanzamiento | Fedora Linux 45 fue lanzado oficialmente el 3 de noviembre de 2026. Para el Dockerfile se utilizará la imagen fedora:45. | [Fedora Linux 45](https://fedoraproject.org/workstation/download/) |
| 2. ¿Hasta cuándo recibe actualizaciones de seguridad? | Fedora 45 tiene previsto recibir actualizaciones de seguridad hasta el 8 de diciembre de 2027, fecha establecida para su fin de soporte. | [Registro oficial de Fedora 45](https://packages.fedoraproject.org/pkgs/fedora-release/fedora-release/fedora-45-updates.html) |
| 3. ¿Qué hardware requiere y funciona en VirtualBox? | Fedora 45 puede instalarse como sistema operativo en VirtualBox. Para Fedora Workstation se recomiendan 4 GB de RAM y 40 GB de almacenamiento. En este proyecto se utilizará como imagen Docker y no será necesario crear una tercera máquina virtual. | [Requisitos de Fedora](https://fedoraproject.org/workstation/download/) |
| 4. ¿Permite el particionado manual? | Sí. Fedora 45 permite realizar particionado manual mediante su instalador Anaconda. Sin embargo, no será necesario para este proyecto porque Fedora se utilizará como imagen base de Docker. | [Particionado manual de Fedora](https://fedoraproject.org/wiki/QA:Testcase_partitioning_custom_standard_partition_ext4) |
| 5. ¿Existe guía oficial para Docker Engine en esta familia? | Sí. Docker proporciona una guía oficial para instalar Docker Engine en Fedora, que incluye Fedora 45. | [Instalación de Docker Engine en Fedora](https://docs.docker.com/engine/install/fedora/) |
| 6. ¿Existe imagen base de Docker Hub para esa versión? | Sí. Docker Hub dispone de la imagen oficial fedora:45, mantenida por Fedora Release Engineering. Esta será la imagen base del Dockerfile del grupo 09. | [Imagen oficial de Fedora en Docker Hub](https://hub.docker.com/_/fedora) |
