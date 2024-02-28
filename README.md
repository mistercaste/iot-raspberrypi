# iot-raspberrypi
Docker compose to bring up my Home Automation Raspberry PI (MQTT sensors, USB camera, etc...). A very personal project in fact ;-) 

## WARNING
Once complete, please remember to setup a password for MotionEye on port `:8765` (initial authentication is just `admin`, without password)

## Pre-requisites
- Raspberry PI (tested on ARM64)
- A static IP address (optional, strongly suggested). Configure it with `nmtui`
- Docker Engine: `curl -sSL https://get.docker.com/ | sh` ([Install Docker Engine on Debian](https://docs.docker.com/engine/install/debian/))
- DHT11 and BMP085 sensors ready to work
- Rasperry PI's I2C interfacing enabled (`raspi-config` -> `Interface options` -> `I2C` -> REBOOT)
- USB camera (check parameters in [docker-compose.yml](https://github.com/mistercaste/iot-raspberrypi/blob/main/docker-compose.yml) by typing in your command line `v4l2-ctl --list-devices`)
- Initial configuration of zigbee2mqtt setup ([zigbee2mqtt - docker](https://www.zigbee2mqtt.io/guide/installation/02_docker.html#manual-cgroup-v1))
- Before running `docker compose up`, please create a `.env` file in the main folder, looking like:
```
MQTT_USERNAME=<my username>
MQTT_PASSWORD=<my password>
```
