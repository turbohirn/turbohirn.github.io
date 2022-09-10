---
layout: page
title: Installation 
level: 3
permalink: /docs/pico/install.html
sort: 5
---


##### Allgemeine Installationsinformationen

Die folgenden Anweisungen sind ohne Admin-Berechtigung und nur über User pi durchzuführen.

1. Bevor turbohirn:pico auf einem Raspberry installiert wird, ist es wichtig die Umgebung, mit folgenden Befehl, zu aktualisieren:  
    `$ sudo apt-get update && sudo apt-get upgrade`
2. Installation von GIT:  
    `$ sudo apt-get install git`
3. Klonen des Projektes aus dem GIT-Repository
    * Master-Branch  
    `$ git clone -b main https://<TOKEN>@github.com/turbohirn/pico.git`
    * Entwicklungs-Branch  
    `$ git clone -b develope https://<TOKEN>@github.com/turbohirn/pico.git`
    * Produktiv-Branch  
    `$ git clone -b deploy https://<TOKEN>@github.com/turbohirn/pico.git`
4. Starten des Setup-Scripts unter /home/pi/pico und Einrichtung der Umgebung.
5. Einrichtung des Crons. Mit diesem Cron wird das Programm nach Reboot wieder neugestartet und auf die letzte Version aus Repository aktualisiert.  
    * `$ crontab -e`
    * Erweiterung um folgenden Zeile:  
    `@reboot bash /home/pi/pico/cronjob.sh`

***

##### Sensoren
Installationsanleitung für 1Wire-Sensoren und für Adafruit DHT-Serie
1. 1-Wire - Installation über Kommandozeile:
    * Alle Module anzeigen lassen  
        `sudo lsmod`
    * *Aktivierung des 1-Wire Buses.*\ Dies erfolgt mit folgenden Befehlen:  
`sudo modprobe wire`  
`sudo modprobe w1-gpio pullup=1`  
`sudo modprobe w1-therm`  
    * *Module in der config.txt.*\ Ab Kernel 3.8 ist die Datei config.txt für das Laden der Module zuständig.  
`sudo nano /boot/config.txt`  
`# Temperatursensor an 1-Wire`  
`dtoverlay=w1-gpio`  
`gpiopin=4`  
Den RaspBerry neu starten.
    * *Funktionsweise prüfen*  
Dies kann mit folgenden Befehlen durchgeführt werden:  
`sudo lsmod`  
`cd /sys/bus/w1/devices`  
`ls cat /sys/bus/w1/devices/28-000005d2e508/w1_slave`  
    * Links:  
        * [Raspberry Pi Setup](https://www.raspberrypi-spy.co.uk/2018/02/enable-1-wire-interface-raspberry-pi/)  
        * [Python Setup](https://forums.raspberrypi.com/viewtopic.php?t=122319)

2. Adafruit DHT, Kommandozeile:  
`sudo pip3 install adafruit-circuitpython-dht`  
`sudo apt-get install libgpiod2`  
Link: [Python Setup](https://learn.adafruit.com/dht-humidity-sensing-on-raspberry-pi-with-gdocs-logging/python-setup)  

