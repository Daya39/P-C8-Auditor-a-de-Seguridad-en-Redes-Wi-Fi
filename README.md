[README.md](https://github.com/user-attachments/files/29232249/README.md)
# Auditoría de Seguridad en Redes Wi-Fi

Práctica académica realizada en entorno controlado con fines educativos.  
**Fecha:** 21 de junio de 2026 | **Herramienta:** Kali Linux | **Interfaz:** wlan0mon (RTL8822CE)

> ⚠️ Esta práctica fue realizada sobre redes propias o con autorización explícita, en el marco de un curso de seguridad informática.

---

## Herramientas utilizadas

| Herramienta | Propósito |
|-------------|-----------|
| airmon-ng | Activar modo monitor |
| airodump-ng | Reconocimiento y captura de handshakes |
| aireplay-ng | Ataque de deautenticación |
| wash | Escaneo de redes con WPS activo |
| hcxdumptool | Captura pasiva en formato PCAPNG |
| hostapd-wpe | Punto de acceso falso (Evil Twin) |
| hashcat | Cracking de hashes por diccionario |

---

## Fases y resultados

| Fase | Técnica | Resultado |
|------|---------|-----------|
| 1 | Reconocimiento (airodump-ng + wash) | 17 APs detectados, 4 con WPS 2.0 sin bloqueo |
| 2 | Captura de handshake WPA2 + deautenticación | Handshake capturado — red `Nexxt_126E58` |
| 3 | Evil Twin con hostapd-wpe | Hash NetNTLMv1 capturado — usuario `christian` |
| 4 | Cracking con hashcat (rockyou.txt) | Contraseña obtenida en < 3 segundos |

---

## Red auditada

| Parámetro | Valor |
|-----------|-------|
| ESSID | Nexxt_126E58 |
| BSSID | C0:25:67:12:6E:59 |
| Canal | 3 |
| Cifrado | WPA2 CCMP PSK |
| Cliente | 60:FF:9E:6D:B9:5E |

---

## Estructura del repositorio

```
auditoria-wifi/
├── README.md
├── 1_reconocimiento/
│   └── airodump_output.md
├── 2_captura_handshake/
│   └── handshake_notes.md
├── 3_ataque_evil_twin/
│   └── hostapd_wpe_output.md
├── 4_cracking/
│   └── hashcat_results.md
└── 5_evidencias/
    └── terminal_completo.txt
```
