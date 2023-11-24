# RED
## COMANDOS
Todos rastran el trafico de la red.
- tcpdump
  - Opciones
  - -n: aparece el numero de las ips
  - -i: indica la interfaz que deseas estudiar
  - net: indicas la red/ip que quieres rastrear
  - Ejemplo: tcpdump -n -i eno1 net 172.26.10.136
- tcptrack: la estudia de manera mas grafica.
  - Opciones
  - -i: indica la interfaz que deseas estudiar
  - Ejemplo: tcptrack -i eno1
- iptraf: Te aparece un menu que te permite estudiar la red con diferentes opciones.

Para ver los puertos abiertos:
- netstat -plunt

