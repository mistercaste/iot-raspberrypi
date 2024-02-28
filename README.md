# iot-raspberrypi
Docker compose to bring up a Raspberry PI for Home Automation.
In fact this is a very personal project :-) 

## WARNING
Once complete, please remember to setup a password for MotionEye on port `:8765` (initial authentication is just `admin`, without password)

## Pre-requisites
- Raspberry PI
  - ZigBee Dongle (e.g. Sonoff)
  - USB Camera (e.g. Logitech)
- Optional static IP address. Setup: `nmtui`
- Docker Engine: `curl -sSL https://get.docker.com/ | sh` (Ref. [Install Docker Engine on Debian](https://docs.docker.com/engine/install/debian/))
- USB camera: setup [docker-compose.yml](https://github.com/mistercaste/iot-raspberrypi/blob/main/docker-compose.yml) by verifying values with `v4l2-ctl --list-devices`
- zigbee2mqtt
  - An MQTT broker configured
  - Initial setup: ([zigbee2mqtt - docker](https://www.zigbee2mqtt.io/guide/installation/02_docker.html))
  - Optional frontend setup on port 8080: ([zigbee2mqtt - frontend](https://www.zigbee2mqtt.io/guide/configuration/frontend.html))

## Sample zigbee2mqtt configuration.yml
Please notice that this way the passwords are stored in clear text.
WARNING - Set `permit_join: false` once the hardware setup is complete!
```
homeassistant: false
permit_join: true
mqtt:
  base_topic: zigbee2mqtt
  server: mqtt://nas.home
  user: ********
  password: ********
serial:
  port: /dev/ttyACM0
frontend:
  port: 8080
  auth_token: ********
```
