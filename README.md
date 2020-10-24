# Stack-InfluxdB-Grafana
# ** Components 

##  InfluxDB - Chronograf - Grafana - Node Red - Portainer - Mosquitto
Coming from Brocaar for Chirpstack server deployment, and from jkehres for -InfluxDB, Chronograf,and Grafana, adding manually Portainer and noder Red from their original websites.
  __________________________________________

Multi-container Docker app built from the following services:

* [InfluxDB](https://github.com/influxdata/influxdb) - time series database
* [Chronograf](https://github.com/influxdata/chronograf) - admin UI for InfluxDB
* [Grafana](https://github.com/grafana/grafana) - visualization UI for InfluxDB

Useful for quickly setting up a monitoring stack for performance testing. Combine with [serverless-artillery](https://github.com/Nordstrom/serverless-artillery) and [artillery-plugin-influxdb](https://github.com/Nordstrom/artillery-plugin-influxdb) to create a performance testing environment in minutes.

  # Docker-compose Node Red / Portainer.
  
  Noder Red: https://nodered.org/docs/getting-started/docker.
  
  Portainer: https://portainer.readthedocs.io/en/stable/deployment.html
  
## Installation:
  * Requirements:
      - Ubuntu server 20.04 (recomneded) - 18.04
      - Docker & Docker-Compose
      
To clone this repository, you need to execute the following commands:

- git clone https://github.com/kaciker/Stack-InfluxdB-Grafana.git

- cd iiOT-All-in-ONE

- docker-compose up

To stop it:

- docker-compose stop

## Ports

The services in the app run on the following ports:
| Host Port | Service |
| - | - |
| 3000 | Grafana |
| 8086 | InfluxDB |
| 1883 | Mosquitto|
| 8888 | Chronograf |
| 1880 | Node Red|
| 9000 | Portainer|

**Notes:** 

#### Chronograf
Note that Chronograf does not support username/password authentication. Anyone can connect to the service and will have full admin access. Consequently, the service is  publically exposed.
To you, to down the service in Portainer if you are not using, or to reinstall the port forwarding 
#### NodeRed
Note that Node Red. Is not configured with autentification. Anyone can connect to the service and will have full admin access. Consequently, the service is  publically exposed.
Soon I will create de docker-compose with autentification.


## To DO
#### Chronograf
Implement Github autentification on docker compose
#### Node Red
Implement autentificaton on docker compose
#### Telegraf
Implement Telegraf
