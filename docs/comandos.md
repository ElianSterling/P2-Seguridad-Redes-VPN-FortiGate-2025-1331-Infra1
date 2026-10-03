# Comandos — Infraestructura 1

> Los secretos no se incluyen.

## FortiGate — interfaces y routing

~~~text
get system interface
get router info routing-table all
get system arp
~~~

## FortiGate — VPN

~~~text
show vpn ipsec phase1-interface
show vpn ipsec phase2-interface
get vpn ipsec tunnel summary
diagnose vpn ike gateway list
diagnose vpn tunnel list
~~~

## FortiGate — captura

~~~text
diagnose sniffer packet any 'host 172.16.10.10 and host 172.16.20.2' 4 0 a
~~~

## Validación

~~~text
ping 172.16.20.2
~~~

Desde los clientes se utilizaron comprobaciones de conectividad y HTTPS para validar el servicio.
