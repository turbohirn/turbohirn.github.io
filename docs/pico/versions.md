---
layout: page
title: Versionierung und GIT
level: 3
permalink: /docs/pico/versions.html
sort: 3
---

Die Struktur der Versionsnummern richtet sich nach folgendem Modell: 
1. **MAJOR**  
Die Major Nummer wird erhöht, wenn die Software zur vorherigen Version inkompatibel wird.
2. **MINOR**  
Die Minor Nummer wird erhöht bei neuen Funktionen der aktuellen Version hinzugefügt werden.
3. **PATCH**  
Die Patch Nummern sind nur Bugfixes, behobene Fehler. Das sind sowohl Softwarefehler als auch Security Updates.
4. **BUILD**  
Diese Angabe repräsentiert den Merge in den Hauptzweig (main) und den davon abgeleiteten Checkout in den Verteilzweig (deploy).

***

## GIT-Repository
{: .display-6 .fs-3 }

Dieses Projekt ist einem Repository bei GitHub abgelegt → https://github.com/turbohirn/pico.git. Die Entwicklungs- und Veröffentlichungszweige gliedern sich wie folgt:  

1. *main* - alle Ressourcen; Backup aller Quellen.  
Klone-URL: `git clone -b main https://<TOKEN>@github.com/turbohirn/pico.git`
2. *deploy* - alle transpilierten Laufzeit-Assets für den Produktiv-Betrieb.  
Klone-URL: `git clone -b deploy https://<TOKEN>@github.com/turbohirn/pico.git`
3. *develope* - Hier befinden sich alle Entwicklungs-Resourcen. Hinweis: Merge-Files für main und deploy müssen immer produktiv transpiliert vorliegen.  
Klone-URL: `git clone -b develope https://<TOKEN>@github.com/turbohirn/pico.git`

