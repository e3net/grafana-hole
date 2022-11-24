# grafana-hole
App mix with pi-hole, unbound, grafana, prometheus, speedtest


# Prerequisites

Install docker
```sh
$ curl  -sSL https://get.docker.com/ | sh
```
Install docker-compose
```sh
$ sudo apt-get install -y libffi-dev libssl-dev
$ sudo apt-get install -y python3 python3-pip
$ sudo pip3 -v install docker-compose
```
# Configuration
Edit .env file to set own password for pihole

Default login/password for grafana: admin/admin

# Installation
```sh
$ git clone https://github.com/e3net/grafana-hole
$ cd grafana-hole
$ docker-compose up -d
```

After pulling and run contenrer the applications will be available at:
- pihole: http://device_ip/admin
- grafana: http://device_ip:3000
- prometheus: http://device_ip:9090

metrics:
- pihole-exporter: http://device_ip:9617
- speedtest-exporter: http://device_ip:9798
- node-exporter: http://device_ip:9100

# Testing
- Debian 11 (bullseye)
- Raspberry pi -> in progress :)

# Used image
Apps:
- pihole: https://hub.docker.com/r/pihole/pihole
- grafana: https://hub.docker.com/r/grafana/grafana
- prometheus: https://hub.docker.com/r/prom/prometheus
- unbound: https://hub.docker.com/r/mvance/unbound

Metrics exporters:
- pihole: https://hub.docker.com/r/ekofr/pihole-exporter
- speedtest-exporter: https://hub.docker.com/r/miguelndecarvalho/speedtest-exporter
- node-exporter: https://hub.docker.com/r/prom/node-exporter

# Dashboards
- pihole: [10176](https://grafana.com/grafana/dashboards/10176-pi-hole-exporter/)
- speedtest:[13665](https://grafana.com/grafana/dashboards/13665-speedtest-exporter-dashboard/)
- node-exporter: [1860](https://grafana.com/grafana/dashboards/1860-node-exporter-full/)

# Provisioning block list
```sh
docker exec -it pihole sqlite3 /etc/pihole/gravity.db "INSERT INTO adlist (address, enabled, comment) VALUES ('https://hole.cert.pl/domains/domains.txt', 1, 'cert');"
```
# Todo
Add provisioning blocking list from file to pihole