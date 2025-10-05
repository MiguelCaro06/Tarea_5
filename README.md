# Análisis de Red con Nmap y Virtualización con QEMU
## Análisis de Red con Nmap

Realizamos un análisis completo de la red local utilizando Nmap para descubrir hosts activos, escanear puertos, identificar servicios y detectar posibles vulnerabilidades.

**Comandos Ejecutados:**
1. Descubrimiento de Hosts en la Red
```
sudo nmap -sn 192.168.1.0/24
```
**Propósito: Identificar todos los dispositivos activos en la red local.**

2. Escaneo Básico del Router
```
sudo nmap -sS -sV 192.168.1.1
```
**Propósito: Analizar los puertos y servicios del router/gateway de la red.**

3. Escaneo Completo Local
```
sudo nmap -sS -sV -sC -O localhost
```
**Propósito: Escaneo exhaustivo de la máquina local incluyendo detección de OS y scripts básicos.**

4. Análisis de Seguridad
```
sudo nmap --script safe 192.168.1.1
```
**Propósito: Ejecutar scripts de seguridad para identificar configuraciones inseguras.**


## Virtualización con QEMU
**Objetivo:**

Instalar y configurar QEMU para crear y ejecutar máquinas virtuales, específicamente con CentOS Stream 10.

**Proceso Realizado:**

1. Instalación de QEMU
```
sudo apt update && sudo apt install qemu-system-x86 qemu-utils qemu-kvm -y
```
2. Creación de Disco Virtual
```
qemu-img create -f qcow2 disk.qcow2 10G
```
Creamos un disco virtual de 10GB en formato qcow2.

3. Configuración de Máquina Virtual
```
qemu-system-x86_64 -hda disk.qcow2 -cdrom /home/miguel/Descargas/CentOS-Stream-10-latest-x86_64-dvd1.iso -boot d -m 2G -vga virtio -display gtk
```
</html>
