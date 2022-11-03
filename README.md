# grafana-hole
App mix with pi-hole, grafana, prometheus, speedtest


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

# Installation
```sh
$ git clone https://github.com/e3net/grafana-hole
$ cd grafana-hole
$ docker-compose up -d
```

After pulling and run contenrer the applications will be available at:
pihole: http://device_ip
grafana: http://device_ip:3000
prometheus: http://device_ip:9090

metrics:
pihole-exporter: http://device_ip:9617
speedtest-exporter: http://device_ip:9798
node-exporter: http://device_ip:9100

# Testing

Debian 11 (bullseye)
Raspberry pi


do sprawdzenia to: https://github.com/danopstech/speedtest_exporter


# used
docker image:
https://github.com/pi-hole/docker-pi-hole
https://github.com/eko/pihole-exporter
grafana
prometheus

dashboards
pihole: 10176
speedtest:13665


node-exporter
id dashboard: 1860
link https://grafana.com/docs/grafana-cloud/quickstart/docker-compose-linux/

speedtest server id list: https://gist.github.com/epixoip/2b8696ed577d584a7f484c006d945051
https://williamyaps.github.io/wlmjavascript/servercli.html