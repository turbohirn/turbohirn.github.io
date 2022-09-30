---
layout: page
title: GPIO Modus
level: 3
permalink: /docs/pico/modus.html
sort: 7
---


## 1. GPIO-Modus konfigurieren
{: .display-6 .fs-3 }
**Modus-Konfiguration aller schaltbarer Pins**  
Bevor mit den GPIOs des Raspberry PI - im weiteren RPI - gearbeitet werden kann, muss der Modus für den jeweiligen Pin festgelegt werden. Dabei wird grundlegend zwischen den Modi IN und OUT unterschieden. Ein einmal festgelegter Pin, wird gespeichert und auch nicht mehr aktiv entfernt. Alle weiteren Änderungen an diesem Pin werden dort gespeichert. Nutzerspezifische Bezeichnungen bleiben dem Pin erhalten, auch wenn sich sein weiterer Betriebszweck ändert.

### Klickpfad und Datentypen:
{: .display-6 .fs-4 }

1. Klick auf ‘Modus Konfiguration’:
Übersicht aller Pins wird nach dem RPI-Schema angezeigt. Nur konfigurierbare Pins werden als klickbar markiert.
2. Klick auf konfigurierbaren Pin:
Es wird ein einfaches Dialogfeld geöffnet. Dort kann über eine SelectBox aus drei Werten ausgewählt werden:
  - **INAKTIV**,  Hierbei wird ein Pin funktionslos gespeichert. Vorraussetzung dafür ist, dass ein bereits gespeicherter Pin über den Modus den Status IN oder OUT verfügt haben. Bezeichner und Beschreibungen bleiben erhalten. Ein so konfigurierter Pin wird nicht in den Listen der Konfiguration angezeigt. Initial kann dieser Status nicht gesetzt werden.  
**Hinweis**: Zusätzlich gesetzte Objekte, wie z.B.: actor, input und state, die ggf. in den weiteren Konfigurationen angelegt wurden, werden automatisch gelöscht.
  - **Eingang** (IN)  
  Siehe Punkt 3. GPIO-Input
  - **Ausgang** (OUT)  
  Hier wird ein Pin mit der Eigenschaft OUT angelegt.  Hinweis: Zusätzlich gesetzte Objekte, wie z.B. input, werden automatisch gelöscht, wenn aus einem anderen Modus in diesen gewechselt wird. 
3. Klick auf Speichern legt den Pin im Dictionary an. GPIO-Aktionen finden hier, unabhängig vom Modus, noch nicht statt.

Datendefinition:  

| Name/Key | Datentyp | INAKTIV | IN | OUT |
| --- | --- | --- | --- | --- | --- |
| pin | Number | GPIO-Vorgabe | | GPIO-Vorgabe |
| gpio | Number | GPIO-Vorgabe | | GPIO-Vorgabe |
| mode | Number | 2 | 1  | 0 |
| state | Number | | | 1 |


<!-- 1 = AN/AUS,  2 = Temperatur,   3 = Luftfeuchte -->