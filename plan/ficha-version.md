# Ficha de verificación de versiones - Grupo 09

**Asignatura:** Sistemas Operativos (2026-2) - Universidad del Valle, sede Yumbo  
**Responsable:** Jaider Stiven Valencia Orobio  
**Fecha de consulta de las fuentes:** 19 de noviembre de 2026  
**Estado:** verificación documental inicial; la instalación real y las capturas se harán en los sprints posteriores.

La combinación asignada por el profesor al grupo 09 es **Manjaro** (VM gráfica), **Ubuntu Server** (VM de consola) y **Fedora** (imagen base del Dockerfile).

## 1. Manjaro XFCE - VM gráfica `g09-grafica`

| Pregunta de la V11 | Respuesta investigada | Fuente |
| --- | --- | --- |
| 1. Versión y fecha de lanzamiento | **Manjaro 26.1.3 XFCE, Bian-May**, imagen publicada el **28 de octubre de 2026**. Para la VM se considera la ISO XFCE con kernel 6.18 LTS. | [Anuncio oficial y enlaces ISO](https://forum.manjaro.org/t/manjaro-26-1-bian-may-released/189526) |
| 2. ¿Hasta cuándo recibe actualizaciones de seguridad? | **No tiene fecha de fin de soporte fija por versión**, porque Manjaro emplea actualizaciones continuas (*rolling release*). Es necesario instalar las actualizaciones del sistema y revisar el soporte del kernel elegido. | [Modelo rolling release](https://wiki.manjaro.org/index.php?title=The_Rolling_Release_Development_Model), [mantenimiento](https://wiki.manjaro.org/index.php?title=System_Maintenance) |
| 3. ¿Qué hardware requiere y funciona en VirtualBox? | Edición **64 bits (x86_64)** y compatible con VirtualBox según la guía de instalación de Manjaro. **Asignación propuesta para el laboratorio, no mínimo oficial:** 2 vCPU, 4 GiB RAM y 35 GiB de disco virtual; se comprobará si el equipo anfitrión lo permite. | [Descargar Manjaro](https://wiki.manjaro.org/index.php?title=Special:MyLanguage/Download_Manjaro), [instalación en VirtualBox](https://wiki.manjaro.org/index.php?title=Installation_Guides) |
| 4. ¿Permite particionado manual? | **Sí.** El instalador permite definir las particiones. En Sprint 1 se deberán crear y evidenciar `/`, `swap` y `/home`, según la V11. | [Guía de particiones](https://wiki.manjaro.org/index.php?title=Special:MyLanguage/Partitioning_Overview_and_Existing_Partition_Tables) |
| 5. ¿Existe guía oficial para Docker Engine en esta familia? | **Docker no publica una guía oficial de Docker Engine específica para Manjaro/Arch** en su lista de plataformas; existen procedimientos comunitarios. La VM prevista para instalar Docker en este proyecto será Ubuntu Server, que sí está cubierta. **No confundir Docker Engine con Docker Desktop.** | [Plataformas de Docker Engine](https://docs.docker.com/engine/install/), [instalación oficial en Ubuntu](https://docs.docker.com/engine/install/ubuntu/) |
| 6. ¿Existe imagen base de Docker Hub para esa versión? | **No se identificó una imagen Docker Official Image específica `manjaro:26.1.3`.** Existen imágenes de terceros, pero no se usarán: la V11 asigna Fedora como base del Dockerfile. | [Buscar imágenes oficiales de Manjaro](https://hub.docker.com/search?badges=official&q=Manjaro&type=image), [imagen oficial Fedora](https://hub.docker.com/_/fedora) |

## 2. Ubuntu Server - VM de consola `g09-consola`

| Pregunta de la V11 | Respuesta investigada | Fuente |
| --- | --- | --- |
| 1. Versión y fecha de lanzamiento | **Ubuntu Server 26.04.1 LTS, Resolute Raccoon**. La versión base 26.04 LTS se publicó el **23 de abril de 2026** y la actualización 26.04.1 el **27 de agosto de 2026**. | [Historial de versiones Ubuntu](https://wiki.ubuntu.com/Releases), [descarga de Ubuntu Server](https://ubuntu.com/download/server) |
| 2. ¿Hasta cuándo recibe actualizaciones de seguridad? | **Hasta abril de 2031** según las notas de Ubuntu 26.04 LTS, durante el período estándar de cinco años. Hay opciones de mantenimiento ampliado con Ubuntu Pro. | [Notas oficiales de 26.04](https://documentation.ubuntu.com/release-notes/26.04/) |
| 3. ¿Qué hardware requiere y funciona en VirtualBox? | Arquitectura **64 bits x86_64**; la página oficial de descarga indica **1,5 GB de RAM y 5 GB de disco** para instalar Ubuntu Server. Puede ejecutarse en VM; **propuesta de laboratorio, no mínimo oficial:** 2 vCPU, 2-4 GiB RAM y 35 GiB de disco virtual. | [Requisitos de Ubuntu Server](https://ubuntu.com/download/server), [Ubuntu en VirtualBox](https://documentation.ubuntu.com/public-images/public-images-how-to/run-an-ova-using-virtualbox/) |
| 4. ¿Permite particionado manual? | **Sí.** El instalador **Subiquity** ofrece configuración personalizada del almacenamiento. Para Sprint 1 se debe seguir la tabla de particiones y las evidencias que exige la V11. | [Documentación de almacenamiento de Subiquity](https://canonical-subiquity.readthedocs-hosted.com/en/latest/howto/configure-storage.html) |
| 5. ¿Existe guía oficial para Docker Engine en esta familia? | **Sí.** Docker documenta la instalación de Docker Engine en **Ubuntu 26.04 LTS (Resolute)** de 64 bits. Se recomienda seguir esa guía al llegar al Sprint 2. | [Instalar Docker Engine en Ubuntu](https://docs.docker.com/engine/install/ubuntu/) |
| 6. ¿Existe imagen base de Docker Hub para esa versión? | **Sí**, la imagen oficial `ubuntu:26.04`. No es la base asignada al Dockerfile del grupo 09, pero existe y está publicada. | [Imagen oficial Ubuntu en Docker Hub](https://hub.docker.com/_/ubuntu) |

## 3. Fedora - imagen base del Dockerfile

| Pregunta de la V11 | Respuesta investigada | Fuente |
| --- | --- | --- |
| 1. Versión y fecha de lanzamiento | **Fedora Linux 45**, publicado el **3 de noviembre de 2026**. Para el Dockerfile se eligió la etiqueta `fedora:45`. | [Anuncio de descarga Fedora 45](https://fedoraproject.org/workstation/download/), [Docker Hub Fedora](https://hub.docker.com/_/fedora) |
| 2. ¿Hasta cuándo recibe actualizaciones de seguridad? | El cronograma de Fedora 45 establece fin de soporte el **8 de diciembre de 2027**; se debe mantener la imagen actualizada mientras esté soportada. | [Registro oficial `fedora-release` de Fedora 45](https://packages.fedoraproject.org/pkgs/fedora-release/fedora-release/fedora-45-updates.html) |
| 3. ¿Qué hardware requiere y funciona en VirtualBox? | **No requiere instalar Fedora como VM**, porque su función en este grupo es ser una imagen de contenedor. La imagen oficial soporta, entre otras, arquitectura `amd64`; se ejecuta mediante Docker Engine sobre el sistema anfitrión correspondiente. | [Arquitecturas de `fedora:45` en Docker Hub](https://hub.docker.com/_/fedora) |
| 4. ¿Permite particionado manual? | **No aplica al uso asignado**: una imagen Docker no tiene instalador de discos como una máquina virtual. No se exige particionar una tercera VM Fedora. | [Imagen oficial Fedora en Docker Hub](https://hub.docker.com/_/fedora) |
| 5. ¿Existe guía oficial para Docker Engine en esta familia? | **Sí.** Docker tiene una guía oficial de instalación para Fedora, que incluye la versión 45. No se instalará Fedora como anfitrión en este proyecto. | [Instalar Docker Engine en Fedora](https://docs.docker.com/engine/install/fedora/) |
| 6. ¿Existe imagen base de Docker Hub para esa versión? | **Sí.** Imagen oficial `fedora:45`, publicada y mantenida por Fedora Release Engineering. Es la base prevista para el Dockerfile del Sprint 3. | [Docker Hub Fedora](https://hub.docker.com/_/fedora) |

## Decisiones y verificaciones pendientes

- **Manjaro:** se escogió XFCE para la VM gráfica. Antes de instalar, comprobar que la ISO elegida se descarga y que el equipo anfitrión dispone de recursos suficientes.
- **Ubuntu Server:** se eligió la LTS reciente 26.04.1 y se verificó que Docker documenta soporte para Ubuntu 26.04.
- **Fedora:** se usará `FROM fedora:45` en el futuro Dockerfile, no se instalará como una tercera máquina virtual.
- **Pruebas prácticas:** todavía no se han realizado. Las capturas, resultados de instalación y solución de problemas se agregarán cuando existan evidencias propias.

