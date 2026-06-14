## Webservice-Kette

```text
[[API]]
↓
Regeln und Struktur der Anfrage

[[XML]]
↓
transportiert die Daten

[[Webservice]]
↓
verarbeitet die Anfrage

[[Puffer]]
↓
hält Anfragen oder Daten kurzfristig bereit

[[Cache]]
↓
speichert wichtige Daten für schnellen Wiederzugriff

[[Rollbackmechanismus]]
↓
setzt bei Fehlern Änderungen zurück
```

### Einfach erklärt

Ein Benutzer oder System startet eine Anfrage.

Die [[API]] gibt vor, welche Daten und Regeln erlaubt sind.

Diese Daten werden oft in [[XML]] verpackt und übertragen.

Der [[Webservice]] verarbeitet die Anfrage.

Falls viele Anfragen gleichzeitig kommen, können sie im [[Puffer]] kurz warten.

Häufig genutzte Daten können im [[Cache]] gespeichert werden, damit sie schneller verfügbar sind.

Wenn ein Fehler passiert, sorgt der [[Rollbackmechanismus]] dafür, dass alles auf den letzten sicheren Zustand zurückgesetzt wird.

