---
layout: page
title: 3. GPIO Input
level: 3
permalink: /docs/pico/input.html
sort: 8
---


## Datenannahme von GPIOs (Modus IN)
{: .display-6 .fs-3 }

Das Entgegennehmen von Eingabezuständen im Modus IN. 
Im Modus IN konfigurierte Pins können Werte von Sensoren und Tastern entgegennehmen. Diese Pins werden mit korrekten Eingabemethoden verknüpft und dann entsprechenden Aktoren zugeordnet. Bei der Verknüpfung wird aktuell unterschieden zwischen:
* An/Aus (onoff)
* Temperatur (temperature)
* Luftfeuchte (humidity)

### Klickpfad und Datentypen:
{: .display-6 .fs-4 }

Klick auf SelectBox öffnet ein Pulldown-Menu.
* Eingabetyp festlegen,  
  Datendefinition:
Hier wird ein Pin mit der Eigenschaft IN angelegt. 
Hinweis: Zusätzlich gesetzte Objekte, wie z.B. actor und state, werden automatisch gelöscht, wenn aus einem anderen Modus in diesen gewechselt wird. (Siehe Hinweis in Punkt 1.2.a → INAKTIV). 



