# P2 — Infraestructura 1
## VPN IPsec FortiGate ↔ FortiGate

**Asignatura:** Seguridad de Redes  
**Proyecto:** P2-Seguridad-Redes-VPN-FortiGate-2025-1331  
**Infraestructura:** 1 de 3  
**Autor:** Elian Sterling  
**Fecha:** octubre de 2026

### 🎥 Video de demostración

**[Ver demostración de Infraestructura 1](https://youtu.be/kekI346Hsyw)**

### Objetivo

Implementar y demostrar una VPN site-to-site IPsec entre dos FortiGate, permitiendo comunicación segura entre una red de usuarios y una red de servidores.

### Arquitectura

![Topología de Infraestructura 1](diagrams/topologia-infraestructura-1.svg)

### Direccionamiento principal

| Equipo / segmento | Dirección | Función |
|---|---|---|
| USER-01 | 172.16.10.10/25 | Cliente de prueba |
| FGT-01 Users | 172.16.10.1/25 | Gateway de usuarios |
| FGT-01 WAN | 203.0.113.2/30 | Peer WAN |
| ISP | 203.0.113.1/30 / 198.51.100.1/30 | Tránsito |
| FGT-02 WAN | 198.51.100.2/30 | Peer WAN |
| FGT-02 Server-LAN | 172.16.20.1/28 | Gateway de servidores |
| WEB-01 | 172.16.20.2/28 | Servidor HTTPS |

### VPN

- Tipo: Site-to-Site IPsec.
- Redes protegidas: **172.16.10.0/25 ↔ 172.16.20.0/28**.
- PSK configurada en ambos extremos.
- Los secretos no se publican en GitHub.

### Validaciones documentadas

- Túnel IPsec establecido.
- USER-01 → WEB-01 mediante ICMP.
- Acceso HTTPS al servidor.
- Verificación de routing y NAT.
- Evidencias gráficas de la configuración y pruebas.

### Contenido del repositorio

- **[Documentación técnica](docs/infraestructura.md)**
- **[Comandos de verificación](docs/comandos.md)**
- **[Evidencias gráficas](docs/evidencias.md)**
- **[Configuraciones sanitizadas](configs/)**
- **[Diagrama](diagrams/topologia-infraestructura-1.svg)**
- **[Capturas](evidencias/)**

### Seguridad

No se publican PSK, contraseñas, tokens ni claves privadas. Los valores sensibles se representan como `<REDACTED>`.
