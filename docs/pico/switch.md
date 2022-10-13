---
layout: page
title: 2. GPIO Switch
level: 3
permalink: /docs/pico/switch.html
sort: 7
---

## Schaltung von Pins im Modus OUT
{: .display-6 .fs-3 }


Die hier geschalteten Pins liegen alle im Modus OUT vor. Beim Schalten (Checkbox-Button) wird der initial gesetzte Wert von 1 auf 0* geändert. Weiterhin ist es möglich, den vorkonfigurierten Pin, mit einem Bezeichner und mit einer Beschreibung zu versehen. Diese Daten werden in einem eigenen Objekt gespeichert, welches auch bei Änderung des Modus erhalten bleibt. Denkbar ist, weitere Daten in diese Objekt abzulegen, die nicht zur eigentlichen Verwendung als GPIO dienen. Eine Löschung dieses Objektes ist nicht vorgesehen.  
**Hinweis**: zu inversiven Schaltzustand: Der Schaltzustand 0 ist nicht aus- sondern eingeschaltet, und umgekehrt wie hier 1 ausgeschaltet ist.