---
layout: page
title: Ziele 
level: 3
permalink: /docs/pico/goals.html
sort: 2
---

Im Client soll es folgende Möglichkeiten geben:
1. GPIOs flexibel  in den Operations-Modus zu versetzen (Modus:  IN/OUT),
2. GPIOs externe Relais zu einfach ein- und auszuschalten (Modus: OUT),
3. GPIOs zeitgesteuert zu schalten (Modus: OUT),  
4. GPIO-Eingangszustände auszuwerten und bei Ereignis GPIOs (wie in Punkt 2) zu schalten  (Modus: IN),
5. Schnittstellen für virtuelle GPIO-Extender und externe Mikrocontroller zur Verfügung zu stellen,
6. Steuerung weiterer Raspberry Pis via Remote-GPIO.

Die Kernkonfiguration des GPIO-Headers befindet sich in einem Python-Dictionary. Die nutzerspezifischen GPIO-Einstellungen werden in einer separaten Stored-JSON-Datei abgelegt und zur Laufzeit mit dem Python-Dictonary angereichert. Diese JSON-Datei befindet sich nicht im GIT-Repository und wird nutzerabhängig erzeugt, wenn noch nicht vorhanden. Damit ist sichergestellt, dass Programmaktualisierungen diese Konfiguration nicht überschreiben oder beeinflussen. Ein Löschung von konfigurierten GPIOs ist nicht vorgesehen.
Hinweis: Die gespeicherten GPIOs mit Status ‘Inactive’ werden in der Stored-JSON belassen, um zukünftige Konfigurationen der Nutzer-Metadaten nicht zu löschen und für eine spätere Verwendung vorzuhalten. Bei Änderungen des Datenmodells im Rahmen der Weiterentwicklung, sollte die Datei stored.json neu erzeugt werden.

Die Steuerung von Pins (Modus OUT) wird von sogenannten Aktoren übernommen. Diese Aktoren steuern Pins entweder über Zeitsteuerungen oder über Eingabewerte. Bei Letzterem müssen Pins (Modus IN) mit einem entsprechenden Eingabe-Trigger konfiguriert sein. Diese Trigger sind aktuell: 
1. An/Aus,
2. Temperatur,
3. Luftfeuchte.

Die Verknüpfung der Aktoren mit den Pins (Modus OUT) erfolgt auf Basis einer 1:n-Verlinkung. Dabei können mehrere Pins von einem Aktor gesteuert werden. Ein einmal zugeordneter Pin (GPIO) kann nicht mit anderen Aktoren verwendet werden. 
