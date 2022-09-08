---
layout: page
title: Installation 
level: 3
permalink: /docs/pico/install.html
sort: 3
---

Die folgenden Anweisungen sind ohne Admin-Berechtigung und nur über User pi durchzuführen.

1. Bevor turbohirn:pico auf einem Raspberry installiert wird, ist es wichtig die Umgebung, mit folgenden Befehl, zu aktualisieren:\
    `$ sudo apt-get update && sudo apt-get upgrade`
2. Installation von GIT:\
    `$ sudo apt-get install git`
3. Klonen des Projektes aus dem GIT-Repository
    * Master-Branch\
    `$ git clone -b main https://<TOKEN>@github.com/turbohirn/pico.git`
    * Entwicklungs-Branch\
    `$ git clone -b develope https://<TOKEN>@github.com/turbohirn/pico.git`
    * Produktiv-Branch\
    `$ git clone -b deploy https://<TOKEN>@github.com/turbohirn/pico.git`
4. Starten des Setup-Scripts unter /home/pi/pico und Einrichtung der Umgebung.
5. Einrichtung des Crons. Mit diesem Cron wird das Programm nach Reboot wieder neugestartet und auf die letzte Version aus Repository aktualisiert.  
    * ```$ crontab -e```
    * Erweiterung um folgenden Zeile:\
    `@reboot bash /home/pi/pico/cronjob.sh`
