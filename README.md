# iot-raspberrypi
Docker compose to bring up my Home Automation Raspberry PI (MQTT sensors, USB camera, etc...). A very personal project in fact ;-) 

## Requisites
- Raspberry PI (tested on ARM64)
- DHT11 and BMP085 sensors (refer to `mistercaste/mqtt-sensors-dockerized` for the configuration)
- USB camera (check parameters in `docker-compose.yml` with `v4l2-ctl --list-devices`)

## CAVEAT
- Remember to setup a password for MotionEye on port `:8765` (initial authentication is just `admin`, without password)
