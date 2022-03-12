# pihole-home

This repository contains the home network setup for pihole and DHCP.

## Setup

Generate certificates for pihole web server:

```
openssl req -x509 -nodes -days 3650 -newkey ec:<(openssl ecparam -name secp384r1) -keyout ./data/certs/pihole.key -out ./data/certs/pihole.crt
```

```
openssl dhparam -out ./data/certs/dhparam-2048.pem 2048
```

## Running

```
docker-compose up
```
