# iot-raspberrypi
Docker compose to bring up my Home Automation Raspberry PI (MQTT sensors, USB camera, etc...). A very personal project in fact ;-) 

## WARNING
Once complete, please remember to setup a password for MotionEye on port `:8765` (initial authentication is just `admin`, without password)

## Requisites
- Raspberry PI (tested on ARM64)
- Docker Engine. Conveniency install for Raspberry PI 4 is: `curl -sSL https://get.docker.com/ | sh` ([Ref. Install Docker Engine on Debian](https://docs.docker.com/engine/install/debian/))
- DHT11 and BMP085 sensors (refer to [mistercaste/mqtt-sensors-dockerized](https://github.com/mistercaste/mqtt-sensors-dockerized) for the configuration)
- USB camera (check parameters in [docker-compose.yml](https://github.com/mistercaste/iot-raspberrypi/blob/main/docker-compose.yml) by typing in your command line `v4l2-ctl --list-devices`)
- Before running `docker compose up`, please create a `.env` file in the main folder, looking like:
```
MQTT_USERNAME=<my username>
MQTT_PASSWORD=<my password>
```
