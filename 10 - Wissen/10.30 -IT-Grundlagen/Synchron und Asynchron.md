# Synchron und Asynchron

## Synchron

Bei einer synchronen Verarbeitung wartet der Aufrufer auf die Antwort.

Ablauf:

```text
Anfrage senden
↓
warten
↓
Antwort erhalten
↓
weiterarbeiten
```

### Beispiel

Ein Webservice wird aufgerufen.

Der Benutzer wartet, bis die Antwort zurückkommt.

Erst danach kann die Anwendung weitermachen.

### Vorteil

- Einfacher Ablauf
- Ergebnis sofort verfügbar

### Nachteil

- Wartezeiten
- Bei langsamen Systemen fühlt sich die Anwendung träge an

---

## Asynchron

Bei einer asynchronen Verarbeitung wird die Anfrage gestartet, aber der Aufrufer arbeitet sofort weiter.

Ablauf:

```text
Anfrage senden
↓
weiterarbeiten
↓
Antwort kommt später
```

### Beispiel

Eine grosse Datei wird importiert.

Der Benutzer erhält:

"Import gestartet."

Während der Import im Hintergrund läuft, kann er weiterarbeiten.

Später erscheint:

"Import erfolgreich abgeschlossen."

### Vorteil

- Keine langen Wartezeiten
- Bessere Performance für Benutzer

### Nachteil

- Komplexer zu programmieren
- Fehler treten eventuell erst später auf

---

## Vergleich

Synchron:

```text
Frage stellen
↓
auf Antwort warten
↓
weiterreden
```

Asynchron:

```text
Nachricht schicken
↓
etwas anderes machen
↓
Antwort später erhalten
```

---

## Zusammenhang mit Webservices

Ein Webservice kann synchron oder asynchron arbeiten.

Synchron:

- Anfrage
- warten
- Antwort

Asynchron:

- Anfrage
- Verarbeitung im Hintergrund
- Antwort oder Status später