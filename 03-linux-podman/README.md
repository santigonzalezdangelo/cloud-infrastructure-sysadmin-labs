# TP3 · Administración de Linux y despliegue de Nginx con Podman

## Descripción

Laboratorio de **virtualización local, administración de Linux y despliegue de contenedores**. Creé una máquina virtual Ubuntu en VirtualBox, instalé **Podman** y **Cockpit** y desplegué un servidor web **Nginx** para comprobar el acceso desde el equipo anfitrión.

**Contexto:** trabajo práctico de Administración de Sistemas de Información, UTN FRLP (2026).

## Tecnologías

- Linux Ubuntu Server
- Oracle VirtualBox
- Podman
- Cockpit y `cockpit-podman`
- Nginx
- Linux CLI y redirección de puertos NAT

## Objetivos

1. Crear un servidor Linux en un entorno virtualizado local.
2. Instalar y administrar servicios con comandos Linux.
3. Gestionar contenedores con **Podman** y la interfaz web **Cockpit**.
4. Desplegar un servidor HTTP y verificar su funcionamiento.
5. Practicar diagnóstico de conectividad y edición de archivos dentro de un contenedor.

## Implementación

### 1. Entorno virtualizado

- Creé una máquina virtual **Ubuntu Server** mediante VirtualBox.
- Asigné los recursos de CPU, memoria y almacenamiento necesarios para el laboratorio.
- Configuré la red de la VM y reglas de **redirección de puertos** para acceder a servicios desde el anfitrión.

### 2. Herramientas de administración

- Actualicé el sistema e instalé **Podman**.
- Instalé y habilité **Cockpit**, junto con la integración **`cockpit-podman`**.
- Accedí a la interfaz de Cockpit desde el navegador utilizando el **puerto 9090**.

### 3. Despliegue del servicio web

- Descargué una imagen de **Nginx** desde el registro de contenedores.
- Creé y ejecuté un contenedor con Podman desde Cockpit.
- Publiqué el servicio HTTP mediante el mapeo de puertos **8080 (anfitrión de contenedor) → 80 (contenedor)** y la redirección correspondiente de VirtualBox.
- Comprobé el funcionamiento de Nginx desde un navegador en **`http://localhost:8080`**.

### 4. Administración del contenedor

- Ingresé al contenedor mediante su terminal.
- Modifiqué el archivo **`index.html`** servido por Nginx.
- Verifiqué que los cambios se reflejaran correctamente en la página web.

## Resolución de problemas

Primero intenté crear la máquina virtual en Azure, pero los recursos disponibles en **Azure for Students** no permitían desplegar una instancia con las características necesarias. Migré el laboratorio a **VirtualBox**.

También debí familiarizarme con la interfaz de Cockpit y su integración con Podman para encontrar las opciones de administración y configuración del contenedor.

## Resultado

- Máquina virtual Linux instalada y operativa.
- **Podman y Cockpit** configurados para administrar contenedores.
- **Nginx** accesible desde el equipo anfitrión.
- Página HTML modificada dentro del contenedor y validada desde el navegador.

## Documentación

📄 [Ver informe técnico del TP3 (PDF)](./TP3.pdf)

El informe incluye capturas de VirtualBox, instalación de Podman y Cockpit, configuración de puertos, ejecución del contenedor y pruebas del servidor web.

> **Aclaración:** la consigna presenta como contexto un despliegue de Db2 Warehouse, pero la implementación documentada en este trabajo corresponde a **Nginx en Podman**. No se afirma haber desplegado Db2.
