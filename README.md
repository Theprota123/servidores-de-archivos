# 🖥️ Servidor de Archivos Samba en Sistema Virtual
<img width="198" height="147" alt="jhon anderson" src="https://github.com/user-attachments/assets/a895f339-5995-4564-bb93-37ffa56bc89b" />
 jhon ortega                                          limberth vallejos

![Samba Server](https://img.shields.io/badge/Samba-4.15.5-orange)
![Ubuntu](https://img.shields.io/badge/Ubuntu-20.04%20LTS-orange)
![License](https://img.shields.io/badge/License-MIT-blue)
![Status](https://img.shields.io/badge/Status-Activo-success)

Una guía completa y visual para implementar un servidor de archivos Samba en un sistema operativo virtual, permitiendo compartir archivos entre diferentes sistemas operativos en una red local.

## 📋 Tabla de Contenidos

- [Descripción del Proyecto](#descripción-del-proyecto)
- [Características](#características)
- [Requisitos del Sistema](#requisitos-del-sistema)
- [Instalación y Configuración](#instalación-y-configuración)
- [Uso del Servidor](#uso-del-servidor)
- [Estructura del Proyecto](#estructura-del-proyecto)
- [Solución de Problemas](#solución-de-problemas)
- [Contribuciones](#contribuciones)
- [Licencia](#licencia)
- [Contacto](#contacto)

## 🚀 Descripción del Proyecto

Este proyecto proporciona una implementación paso a paso de un servidor de archivos Samba ejecutándose en un sistema operativo virtual. La solución permite:

- Compartir archivos entre sistemas Windows, Linux y macOS
- Acceso mediante IP del router local (ej: `\\192.168.0.101`)
- Autenticación de usuarios y control de permisos
- Interfaz web educativa con documentación interactiva

### 🎯 Objetivos del Proyecto

- **Educativo**: Enseñar conceptos de redes y servidores de archivos
- **Práctico**: Proporcionar una solución funcional para uso personal o empresarial
- **Accesible**: Guía visual con ejemplos prácticos y código listo para usar

## ✨ Características

### 🔧 Características Técnicas
- **Servidor Samba** completamente configurado
- **Acceso por IP** desde cualquier dispositivo en la red local
- **Gestión de usuarios** y permisos personalizables
- **Firewall configurado** para seguridad óptima
- **Inicio automático** del servicio al arrancar el sistema

### 🎨 Características de la Documentación
- **Interfaz web responsive** con diseño 4K
- **Animaciones y efectos visuales** interactivos
- **Código ejecutable** con botones de copiar
- **Guía paso a paso** con progreso visual
- **Solución de problemas** integrada

## 📋 Requisitos del Sistema

### Requisitos Mínimos
- **Sistema Virtual**: VMware, VirtualBox o Hyper-V
- **Sistema Operativo**: Ubuntu Server 20.04 LTS o superior
- **RAM**: 1 GB mínimo (2 GB recomendado)
- **Almacenamiento**: 10 GB de espacio libre
- **Red**: Conexión a internet y red local

### Requisitos Recomendados
- **Procesador**: 2 núcleos o más
- **RAM**: 4 GB para mejor rendimiento
- **Almacenamiento**: 20 GB SSD
- **Sistema Anfitrión**: Windows 10/11, macOS o Linux

## 🛠️ Instalación y Configuración

### Prerrequisitos
1. Instalar software de virtualización (VirtualBox recomendado)
2. Descargar imagen ISO de Ubuntu Server
3. Crear máquina virtual con configuración adecuada

### Pasos de Instalación Rápidos

```bash
# 1. Actualizar sistema
sudo apt update && sudo apt upgrade -y

# 2. Instalar Samba
sudo apt install samba samba-common-bin -y

# 3. Configurar firewall
sudo ufw allow samba

# 4. Crear directorio compartido
sudo mkdir -p /srv/samba/share
sudo chmod -R 0777 /srv/samba/share
sudo chown -R nobody:nogroup /srv/samba/share

# 5. Configurar Samba
sudo nano /etc/samba/smb.conf
