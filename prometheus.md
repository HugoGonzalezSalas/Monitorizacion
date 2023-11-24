# 1. PROMETHEUS  
## 1.1.- Que es Prometheus?
- Aplicación OpenSource para monitorizar sistemas y servicios.
- Recopilación de métricas
- Almacenamiento de series temporales
- Consultas y visualización de datos
- Alertas y notificaciones
- Escalabilidad y extensibilidad

Es una solución de monitorización y alerta diseñada especialmente
para entornos dinámicos. Ofrece almacenamiento local de series temporales y
una interfaz web para consultas y visualizaciones.

## 1.2.- Node Exporter
Un exporter son los programas encargados de obtener las métricas y
formatearla para que Prometheus pueda leerlas

Node-Exporter es un exporter (librería) que se encarga de extraer métricas
relacionadas con hardware y el kernel. Por ejemplo:
- arp Expone las estadísticas ARP de /proc/net/arp.
- cpu
- diskstats Expone las métricas de I/O de los discos.
- entropy Expone la entropía disponible (muy importante para la
criptografía).
- filesystem Expone las estadísticas de los sistemas de ficheros, como
el espacio en disco usado, etc.
- hwmon Expone los sensores de hardware de /sys/class/hwmon/
- loadavg Expone el promedio de carga del nodo.
- meminfo Expone las estadísticas de la RAM.
- netclass Expone la información de las interfaces de red
de /sys/class/net/
- netdev Más estadísticas de red, como los bytes transferidos, etc.
## 1.3.- ¿Qué es grafana?
Es una herramienta poderosa para visualizar y analizar datos.
odemos integrarlo con Prometheus.
Las principales características de Grafana son:
- Visualización de datos.
- Soporte para múltiples fuentes de datos: Prometheus, InfluxDB, MySQL,
- PostgreSQL, AWS CloudWatch, Microsoft SQL Server, entre otros.
- Creación de paneles dinámicos.
- Alertas y notificaciones.
- Interfaz intuitiva.
- Comunidad

## 2. Instalacion y Configuración.

- apt install prometheus
- systemctl daemon-reload
- systemctl status prometheus
- systemctl list-unit-files -t service | grep "prometheus"
- apt install -y apt-transport-htpps
- apt install -y software-properties-common wget
- wget -q -O - https://packages.grafana.com/gpg.key | apt-key add -
- echo "deb https://packages.grafana.com/oss/deb stable main" | tee -a
/etc/apt/sources.list.d/grafana.list
- apt update
- apt install grafana

###NOT starting on installation, please execute the following statements
to configure grafana to start automatically using systemd
sudo /bin/systemctl daemon-reload
sudo /bin/systemctl enable grafana-server
###You can start grafana-server by executing
sudo /bin/systemctl start grafana-server

- systemctl daemon-reload
- systemctl enable grafana-server
- systemctl start grafana-server.service
- 
