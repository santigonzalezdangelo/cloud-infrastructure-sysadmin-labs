# Laboratorios de infraestructura cloud y administración de sistemas

Repositorio de proyectos académicos desarrollados en **Administración de Sistemas de Información (UTN Facultad Regional La Plata, 2026)**. Reúne prácticas de aprovisionamiento de infraestructura en Microsoft Azure, administración de Windows Server y Active Directory, virtualización local y despliegue de servicios en contenedores.

El objetivo es documentar **qué configuré, cómo comprobé que funcionaba y qué problemas resolví**. Todos los entornos descriptos son laboratorios académicos, no sistemas de producción.

## Proyectos

| Laboratorio | Qué implementé | Tecnologías principales |
| --- | --- | --- |
| [01 · Máquinas virtuales en Azure](./01-azure-virtual-machines/) | Despliegue de Windows Server y Ubuntu Server; acceso remoto; configuración inicial de AD DS; gestión de recursos. | Azure, Windows Server, Ubuntu, RDP, SSH, NSG |
| [02 · Active Directory y GPO](./02-active-directory/) | Dominio corporativo simulado, 14 unidades organizativas, usuarios, equipos y políticas de seguridad verificadas. | Azure, Windows Server, Active Directory, GPO |
| [03 · Linux, Podman y Cockpit](./03-linux-podman/) | Servidor Ubuntu en VirtualBox, administración web y despliegue de Nginx en un contenedor. | Linux, VirtualBox, Podman, Cockpit, Nginx |

## Conocimientos puestos en práctica

- **Infraestructura cloud:** creación y dimensionamiento de máquinas virtuales y organización mediante Resource Groups en Microsoft Azure.
- **Administración de sistemas:** configuración de Windows Server y Ubuntu Server; conexión y diagnóstico mediante RDP y SSH.
- **Identidades y permisos:** instalación de Active Directory Domain Services, creación de un dominio, usuarios, equipos y unidades organizativas; aplicación de GPO.
- **Redes:** configuración básica de reglas de entrada y redirección de puertos en entornos virtualizados.
- **Virtualización y contenedores:** uso de VirtualBox y despliegue de Nginx mediante Podman, administrado con Cockpit.
- **Documentación y resolución de problemas:** registro de procedimientos, verificaciones y dificultades encontradas.

## Estructura

```text
.
├── README.md
├── 01-azure-virtual-machines/
│   ├── README.md
│   └── TP1.pdf
├── 02-active-directory/
│   ├── README.md
│   └── TP2.pdf
└── 03-linux-podman/
    ├── README.md
    └── TP3.pdf
```

Cada carpeta incluye un resumen técnico y, una vez incorporado, el **informe del trabajo práctico en PDF** con capturas de pantalla y el procedimiento seguido.

## Alcance y consideraciones

Estos proyectos reflejan **experiencia práctica académica**. No implican administración de entornos productivos ni experiencia con servicios no utilizados en los trabajos, como AWS, Zabbix o sistemas de backup empresarial.

> **Antes de publicar los informes:** revisar las capturas y ocultar contraseñas, datos de cuentas, direcciones IP públicas y otros identificadores sensibles. En un entorno de producción, los puertos de administración deben tener accesos restringidos.
