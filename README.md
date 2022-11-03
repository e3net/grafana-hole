# grafana-hole
App mix with pi-hole, grafana, prometheus, speedtest


# prerequisites
install docker

instal docker-compose

# instalation
git clone https://github.com/e3net/grafana-hole

cd grafana-hole
docker-compose up -d



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