# 3 Data Communication Basics

## Broker-Based Data Communication (pub/sub)

pub: publish
sub: subscribe

### Terminologies

- topic: the subject of interest
- message: a piece of data for a certain type
- publishers: programs that publishes messages of certain topics
- subscribers: programs that subscribes to certain topics
- broker: a program that helps forward messages from publishers to subscribers

### Message Delivery Semantics

1. Each message will be delivered to all who subscribed to the corresponding topic (example: MQTT)
2. Each message will be delivered to only one of the corresponding subscribers (example: MSQ)

## MQTT Protocol

Implementation for MQTT clients
- https://github.com/mqtt/mqtt.org/wiki/libraries
- https://pypi.org/project/paho-mqtt/

### Terminology


