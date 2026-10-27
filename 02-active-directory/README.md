# TP2 · Administración de dominio con Active Directory y GPO

## Descripción

Implementación de un **dominio de Active Directory sobre Windows Server desplegado en Microsoft Azure** para simular la administración centralizada de identidades, equipos y políticas de seguridad de una organización con **14 departamentos**.

**Contexto:** trabajo práctico de Administración de Sistemas de Información, UTN FRLP (2026).

## Tecnologías

- Microsoft Azure y Azure Virtual Machines
- Windows Server
- Active Directory Domain Services (AD DS)
- Active Directory Users and Computers
- Group Policy Management (GPO)
- RDP y `gpupdate /force`

## Objetivos

1. Configurar un servidor Windows como **controlador de dominio**.
2. Crear un dominio y organizar recursos por departamentos.
3. Administrar cuentas de usuario y objetos de equipo.
4. Definir y comprobar políticas de grupo para restringir funciones del sistema.
5. Documentar la implementación y solucionar incidencias de acceso.

## Implementación

### 1. Servidor y dominio

- Desplegué una máquina virtual Windows Server en **Microsoft Azure**.
- Accedí al servidor por **RDP** e instalé el rol **AD DS**.
- Promoví el servidor a controlador de dominio.
- Creé el dominio **`ADRComputing.local`**.

### 2. Estructura organizativa

- Creé **14 unidades organizativas (OU)**, una por cada departamento de la empresa simulada.
- Registré **dos usuarios por departamento** y los objetos de equipo asociados, siguiendo la estructura del ejercicio.

### 3. Políticas de grupo

Configuré y documenté una prueba de GPO para el área de **Tesorería**:

- Restricción de acceso al **Panel de control y a Configuración**.
- Restricción de acceso al **símbolo del sistema (CMD)**.
- Actualización de políticas mediante **`gpupdate /force`**.

### 4. Comprobación de políticas

Inicié sesión con un usuario del dominio y comprobé que las restricciones impedían abrir el Panel de control y CMD, tal como estaba previsto.

## Resolución de problemas

Durante la verificación, el usuario del dominio no podía iniciar sesión remotamente porque **no tenía los permisos de acceso necesarios**. Revisé la configuración del servidor, ajusté la pertenencia del usuario al grupo correspondiente, actualicé las políticas y repetí la prueba hasta conseguir el acceso y validar las GPO.

Este incidente permitió practicar diagnóstico de **permisos, autenticación y acceso remoto**.

## Resultado

- Dominio de Active Directory configurado.
- **14 OU** creadas con usuarios y equipos asociados.
- Políticas de seguridad configuradas y **comprobadas con una cuenta del dominio**.
- Problema de acceso remoto identificado y resuelto durante la validación.

## Documentación

📄 [Ver informe técnico del TP2 (PDF)](./TP2.pdf)

El informe contiene las capturas de creación del dominio, unidades organizativas, cuentas de usuario, GPO, pruebas de restricciones y *troubleshooting*.

> **Alcance:** laboratorio académico en una empresa simulada. Las restricciones mostradas son un ejercicio de administración de políticas, no una política de seguridad corporativa completa.
