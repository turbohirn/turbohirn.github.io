---
layout: page
title: Grundlegendes zum Programm
level: 3
permalink: /docs/pico/basics.html
sort: 5
---

##### Einleitung
Die Daten werden im JSON-Format in der Datei /cfg/stored.json abgelegt. Diese Datei wird beim Start des Programms, mit folgender Datendefinition, angelegt.
Datendefinitionen:

| Name/Key | Datentyp | Funktion/Kommentar |
| store | Dictionary | Wurzelelement |
| store/pins | Dictionary | Liste aller definierter Pins (ListItems) |
| store/actors | Dictionary | Ablage des initialen Frontend-Users und weiterer Nutzer. |
| store/user | Dictionary | Ablage des initialen Frontend-Users und weiterer Nutzer. Variablenliste mit den Feldern für Benutzer und Passwort, Datentyp String, Standardwert für ersten Listeneintrag: usr = ‘root’, pwd = ‘’|

<br/>

##### Programmstart
Wurde bereits eine Reihe von Pins (im Modus OUT) konfiguriert, werden diese beim Programmstart gesondert behandelt. Dies ist besonders bei Neustarts, Systemumzug, etc. notwendig. Bevor der Webserver gestartet wird, werden die gespeicherten Pins zyklisch gestartet. Das bedeutet im Detail: Jeder Pin im Modus OUT wird mit dem Status gestartet, in dem er zuletzt gespeichert wurde. Um Überlastungen des Stromnetzes bei gesteuerten Relais mit Stromschaltungen zu verhindern, werden diese mit einem Abstand von einer Sekunde separat gestartet. Dieser Zyklus kann in der Konfiguration angepasst werden. Sinnvoll ist dies, wenn Stromverbraucher beim Einschalten länger als eine Sekunde benötigen.
Konfigurierte Zeitsteuerungen und Steuerungen über die definierten Eingangszustände  werden mit der python-internen HeartBeat-Methode automatisch gestartet.

