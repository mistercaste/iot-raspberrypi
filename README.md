# iot-raspberrypi
Docker compose to bring up my Home Automation Raspberry PI (MQTT sensors, USB camera, etc...). A very personal project in fact ;-) 

## WARNING
Once complete, please remember to setup a password for MotionEye on port `:8765` (initial authentication is just `admin`, without password)

## Pre-requisites
- Raspberry PI
- Optional static IP address. Setup: `nmtui`
- Docker Engine: `curl -sSL https://get.docker.com/ | sh` (Ref. [Install Docker Engine on Debian](https://docs.docker.com/engine/install/debian/))
- USB camera: setup [docker-compose.yml](https://github.com/mistercaste/iot-raspberrypi/blob/main/docker-compose.yml) by verifying values with `v4l2-ctl --list-devices`
- Setup zigbee2mqtt
-- Initial setup: ([zigbee2mqtt - docker](https://www.zigbee2mqtt.io/guide/installation/02_docker.html))
-- Frontend setup on port 8080: ([zigbee2mqtt - frontend](https://www.zigbee2mqtt.io/guide/configuration/frontend.html))
