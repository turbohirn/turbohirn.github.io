---
layout: page
title: Programmkonfiguration
level: 3
permalink: /docs/pico/config.html
sort: 6
---


##### Felder der Konfiguration
In der Datei python/config/settings.py werden folgende Standardwerte abgelegt.

| Name/Key | Datentyp | Funktion/Kommentar |
| system | Dictionary | Systemweite Einstellungen |
| controller | Dictionary | Liste aller definierter Pins (ListItems) |
| settings | Dictionary | Ablage des initialen Frontend-Users und weiterer Nutzer. <br/>**pintypes** → Einstellungen der GPIO-Farben, -Labels und Pin-Adressierungen, <br/>**pins** → Basiskonfiguration der schaltbaren GPIOs|
| svglib | Dictionary | Bibliothek der SVG-Grafiken, |

<br/>
