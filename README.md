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



do sprawdzenia to: https://github.com/danopstech/speedtest_exporter


# used
docker image:
https://github.com/pi-hole/docker-pi-hole
https://github.com/eko/pihole-exporter
grafana
prometheus

dashboards
pihole:
speedtest:13665