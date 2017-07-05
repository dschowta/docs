# How to run GOST on raspberry pi

## Version

Check version of your Raspberry Pi:

This document is written for Raspian Jessie:

```
pi@raspberrypi:~ $ lsb_release -a
No LSB modules are available.
Distributor ID:	Raspbian
Description:	Raspbian GNU/Linux 8.0 (jessie)
Release:	8.0
Codename:	jessie
pi@raspberrypi:~ $ 
```

## Install Docker

```
$ curl -sSL get.docker.com | sh
```

## Install GOST

```
$ wget https://raw.githubusercontent.com/gost/docker-compose/master/docker-compose-rpi.yml
$ docker-compose -f docker-compose-rpi.yml up
```

## Check installation

- Dashboard: In browser go to http://raspberrypi:8080