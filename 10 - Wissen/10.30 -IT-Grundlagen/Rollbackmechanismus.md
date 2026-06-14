# Rollbackmechanismus

## Definition

Ein Rollbackmechanismus setzt Änderungen zurück, wenn während eines Prozesses ein Fehler auftritt.

Das System kehrt dabei in den letzten stabilen Zustand zurück.

Das Ziel ist, unvollständige oder fehlerhafte Daten zu vermeiden.

---

## Einfach erklärt

Stell dir vor:

Du änderst 10 Datensätze.

Nach dem 7. Datensatz tritt ein Fehler auf.

Ohne Rollback:

- 7 Datensätze geändert
- 3 Datensätze nicht geändert

→ Das System ist inkonsistent.

Mit Rollback:

- Alle 7 Änderungen werden zurückgenommen.
- Das System bleibt sauber.

---

## Beispiel im Webservice

Ein Webservice startet eine Verarbeitung:

Webservice startet  
↓  
Daten werden geändert  
↓  
Fehler tritt auf  
↓  
Rollback startet  
↓  
Alle Änderungen werden rückgängig gemacht

So bleibt der ursprüngliche Zustand erhalten.

---

## Beispiel in Datenbanken

Eine Überweisung:

Konto A → -100 CHF  
Konto B → +100 CHF

Wenn zwischen den beiden Schritten ein Fehler passiert:

Ohne Rollback:

- Konto A verliert Geld
- Konto B erhält nichts

Mit Rollback:

- Konto A bekommt die 100 CHF zurück.

Alles bleibt korrekt.

---

## Beispiel bei Updates

Ein Systemupdate wird installiert.

Während der Installation tritt ein Fehler auf.

Rollback:

- entfernt die neuen Änderungen
- stellt die alte funktionierende Version wieder her

---

## Warum ist Rollback wichtig?

Rollback schützt vor:

- halbfertigen Änderungen
- Datenverlust
- inkonsistenten Daten
- beschädigten Systemzuständen

---

## Zusammenhang mit anderen Begriffen

[[API]]  
↓  
liefert Regeln

[[XML]]  
↓  
liefert Daten

[[Webservice]]  
↓  
verarbeitet Anfrage

Fehler  
↓  
Rollback

Rollback ist oft der Sicherheitsmechanismus am Ende eines Prozesses.

---

## Merksatz

Rollback bedeutet:

Wenn etwas schiefgeht, geht das System einen Schritt zurück.
