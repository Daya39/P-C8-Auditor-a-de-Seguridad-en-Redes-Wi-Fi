# 🔐 Auditoría de Seguridad en Redes Wi-Fi

> **⚠️ ADVERTENCIA**: Este repositorio es exclusivamente para fines educativos y de concienciación sobre seguridad. El uso indebido de estas técnicas en redes sin autorización explícita es ilegal.

## 📋 Descripción

Este proyecto documenta una práctica completa de **auditoría de seguridad en redes Wi-Fi** utilizando herramientas de Kali Linux. Se evaluaron vulnerabilidades en redes WPA/WPA2-PSK y WPS, aplicando técnicas de:

- Captura y análisis de handshakes
- Cracking de contraseñas con diccionarios y reglas
- Ataques WPS (Pixie Dust)
- Ataques de Evil Twin con captura de credenciales

## 🎯 Objetivos

- ✅ Evaluar la robustez de contraseñas WPA2
- ✅ Identificar vulnerabilidades en WPS
- ✅ Demostrar ataques de captura de credenciales
- ✅ Proporcionar recomendaciones de seguridad

## 🛠️ Herramientas Utilizadas

| Herramienta | Versión | Función |
|-------------|---------|---------|
| airmon-ng   | 1.7     | Gestión de modo monitor |
| airodump-ng | 1.7     | Escaneo y captura |
| aireplay-ng | 1.7     | Inyección de paquetes |
| aircrack-ng | 1.7     | Cracking WPA/WPA2 |
| reaver      | 1.6.6   | Ataque WPS |
| hcxdumptool | 7.0.0   | Captura PMKID/Handshake |
| hashcat     | 7.1.2   | Cracking de hashes |
| hostapd-wpe | -       | AP falso para captura |

## 🚀 Inicio Rápido

### Prerrequisitos

# Sistema operativo
Kali Linux

# Hardware
Adaptador Wi-Fi compatible con modo monitor y inyección
(Recomendado: ALFA AWUS036ACH, TP-Link TL-WN722N)

# Diccionarios
/usr/share/wordlists/rockyou.txt (descomprimido)
