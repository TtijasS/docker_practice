FROM alpine:latest

RUN apk update && apk add openvpn iproute2 bash

COPY client1.ovpn /client.ovpn

CMD ["openvpn", "--config", "/client.ovpn"]