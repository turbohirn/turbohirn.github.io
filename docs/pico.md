---
layout: page
title: PICO
desc: Ein Raspberry Projekt zur Steuerung von stromabhängigen Verbrauchern anhand von Eingangs- und Zeitwerten.
permalink: /docs/pico/index.html
level: 2
sort: 1
---



Schaffung der Möglichkeit einer freie Konfiguration von GPIOs des Raspberry Pis via App, Mobile und Desktop. Dabei soll für jeden einzelnen programmierbaren GPIO-PIN der Modus individuell festgelegt werden können. Dies soll durch eine webbasierte und hostnahe Applikation bewerkstelligt werden.  

Der Plan ist, die Applikation in nur zwei Ausführungsschichten (Excution Level 1 und 2, kurz EL1 und EL2) anzulegen. Die erste Schicht ist ein  python-basiertes Script, welches direkt in einer Shell gestartet werden kann. Diese Schicht stellt Web- und WebSocket-Server bereit und führt host-nahe Kommandos, wie z.B. das Steuern von GPIOs und zyklischen Routinen, aus. Darunter ist in erster Linie die Steuerung und die Entgegennahme von GPIO-Zuständen zu verstehen.

Die zweite Schicht wird in einer browserbasierten Oberfläche (Client) gestartet und bereitet die Daten zum Abspeichern für die erste Schicht auf. Das kann ein Client-Browser oder eine App mit Framed-HTML-Funktion sein. Die Kommunikation zwischen den Schichten wird via WebSocket realisiert. Der Server ist in Python geschrieben und der Client ist in React JS verfasst.