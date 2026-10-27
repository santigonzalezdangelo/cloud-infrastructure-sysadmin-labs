# TP1 · Despliegue de máquinas virtuales en Microsoft Azure

## Descripción

Laboratorio de **aprovisionamiento y configuración inicial de infraestructura cloud** con Microsoft Azure. Desplegué dos máquinas virtuales, una con **Windows Server 2025 Datacenter** y otra con **Ubuntu Server 24.04 LTS**, configuré el acceso remoto e instalé **Active Directory Domain Services (AD DS)** en Windows Server.

**Contexto:** trabajo práctico de Administración de Sistemas de Información, UTN FRLP (2026).

## Tecnologías

- Microsoft Azure y Azure for Students
- Azure Virtual Machines y Resource Groups
- Windows Server 2025 Datacenter
- Ubuntu Server 24.04 LTS
- Active Directory Domain Services (AD DS)
- Conexiones remotas RDP y SSH
- Reglas de seguridad de red (NSG)

## Objetivos

1. Crear y dimensionar máquinas virtuales con sistemas operativos distintos.
2. Acceder a Windows Server y Ubuntu Server de forma remota.
3. Instalar y configurar los servicios iniciales de Active Directory.
4. Administrar el estado de los recursos para evitar consumo innecesario de créditos del laboratorio.

## Implementación

### 1. Organización y aprovisionamiento en Azure

- Utilicé la suscripción educativa **Azure for Students**.
- Creé un **Resource Group** para organizar los recursos del trabajo.
- Seleccioné región, imagen del sistema operativo y tamaño de las máquinas virtuales según la disponibilidad ofrecida por Azure.
- Desplegué instancias de laboratorio de **2 vCPU y 4 GiB de RAM**.

### 2. Servidor Windows

- Implementé una máquina virtual con **Windows Server 2025 Datacenter**.
- Configuré las credenciales iniciales y accedí al equipo mediante **RDP**.
- Instalé el rol **Active Directory Domain Services** desde Server Manager.
- Promoví el servidor a **controlador de dominio** y verifiqué la creación del dominio de laboratorio `tp1.local`.

### 3. Servidor Linux

- Implementé una máquina virtual con **Ubuntu Server 24.04 LTS**.
- Habilité la conexión de administración y accedí desde una terminal de Windows mediante **SSH**.
- Trabajé con la configuración de reglas de entrada de red desde Azure.

### 4. Gestión de recursos

- Detuve las máquinas virtuales al finalizar las pruebas para reducir el consumo de créditos disponibles en la suscripción educativa.

## Validación

- Implementación de ambas máquinas virtuales completada en Azure.
- Acceso remoto realizado por **RDP** a Windows Server y por **SSH** a Ubuntu Server.
- Instalación de **AD DS** y promoción del servidor Windows a controlador de dominio.

## Resolución de problemas

Algunas regiones no ofrecían los tamaños de instancia previstos. Probé distintas combinaciones de **región y tamaño de VM** hasta encontrar recursos disponibles. Para completar la configuración de Active Directory, consulté documentación y otras fuentes técnicas para resolver pasos que no estaban detallados en la consigna.

## Documentación

📄 [Ver informe técnico del TP1 (PDF)](./TP1.pdf)

El informe incluye capturas de la creación de recursos, conexiones remotas, configuración de Active Directory y sección de *troubleshooting*.

> **Nota de seguridad:** las reglas de ingreso del laboratorio no constituyen una configuración recomendada para producción. Conviene limitar el origen de SSH/RDP y revisar la exposición de puertos antes de reutilizar este procedimiento.
