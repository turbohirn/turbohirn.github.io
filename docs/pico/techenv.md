---
layout: page
title: Technik und Umgebung 
level: 3
permalink: /docs/pico/techenv.html
sort: 4
---

#### Hardware
Für den Betrieb ist ein Raspberry Pi, ab Verion 3 notwendig. Auflistung der notwendigen Hardware (Testumgebung):
1. Raspberry Pi ab 3b+ (Menge = 1), Funktion: Hostsystem mit Datenspeicher
2. GeeekPi GPIO Screw Terminal Hat, Funktion: Optische Anzeige der konfigurierten Pins
Mindestvoraussetzungen:
* Raspberry Pi Zero mit 512MB RAM,
* microSD mit 32 GB,


#### Software
Die Applikation wird in JavaScript für das Frontend und Python für das Backend umgesetzt.
1. Frontend  
Bei der JS-Frontend-Programmierung kommen folgende Bibliotheken zum Einsatz:
    * Bootstrap 5.x
    * react.js
    * react-bootstrap
    * socket-io
2. Backend/Server  
Für das Backend und werden folgende Umgebungen und Bibliotheken benötigt:
    * Python ab 3.7.x  
    Python Bibliotheken:
        * socket-io,
        * aiohttp,
        * asyncio,
        * aiohttp_compress,
    
    Das Bash-Script setup.sh installiert auf Wunsch alle Updates und Bibliotheken.

#### Entwicklungsumgebung

Node.js Installation und Update  
Zur Einrichtung auf einem macOS- oder Linux-Desktop  
Installationsdatei: [Nodes.js für Mac](https://nodejs.org/en/download/)  
Update von Node.js
1. `$ sudo npm cache clean -f`
2. `$ sudo npm install -g n`
3. `$ sudo n stable`
4. `$ # node -v`

Aktualisierung des NPM-Package managers
1. `$ sudo npm install -g npm@latest`

Python3-Befehle auf RPI
* Kontrolle was läuft:  
`$ ps aux | grep -i python`
* Python-Server-Prozess hart beenden:  
`$ killall python oder $ pkill -f run.py`
