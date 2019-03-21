# An eclipse-mosquitto docker container

Does basic mosquitto but also persists log / data - original application is for Azure IoT Edge.

Alternative base image is [official Eclipse Mosquitto MQTT Broker Docker image](https://hub.docker.com/_/eclipse-mosquitto/).

## Usage
Pretty simple just ...

### Build and run

```
docker-compose build
docker-compose up -d
```

### Testing

Try the [MQTT client](http://mqttfx.org/) to connect to the Mosquitto MQTT Broker. Use `127.0.0.1:1883` for a local environment.

Or use official `mosquitto_pub` and `mosquitto_sub` utilities for publishing and subscribing.

```
# Subscribe to topic.
mosquitto_sub -h localhost -t test 
# Publish a message.
mosquitto_pub -h localhost -t test -m "hello."
```
