FROM hypriot/rpi-alpine

MAINTAINER app4rpi <app4rpi@outlook.com> \
        Description="MQTT server over Alpine Linux."
#
RUN apk update
RUN apk --no-cache add mosquitto mosquitto-clients
RUN echo "listener 1883" >> /etc/mosquitto/mosquitto.conf
RUN echo "protocol mqtt" >> /etc/mosquitto/mosquitto.conf
RUN echo "listener 9001" >> /etc/mosquitto/mosquitto.conf
RUN echo "protocol websockets" >> /etc/mosquitto/mosquitto.conf
# Expose MQTT port
EXPOSE 1883 9001

ENV PATH /usr/sbin:$PATH

ENTRYPOINT ["/usr/sbin/mosquitto"]
