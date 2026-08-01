- [Backend](#backend)

### Backend

| Bereich | Inhalt |
|---|---|
| 🇬🇧 Englisch | Backend |
| 🇩🇪 Deutsch | Serverseitiger oder nicht sichtbarer Teil einer Anwendung |
| 🎯 Wozu dient das? | Das Backend verarbeitet Anfragen, führt fachliche Regeln aus, greift auf Datenbanken zu und liefert Ergebnisse an das Frontend oder andere Systeme zurück. |
| 🧠 Merksatz | **Das Backend arbeitet im Hintergrund und verarbeitet die Daten.** |

<details>
<summary>💡 Beispiel</summary>

Eine Benutzerin sucht im Frontend nach einer Person.

Das Backend:

1. nimmt die Anfrage entgegen
2. prüft die Berechtigung
3. kontrolliert die Suchparameter
4. fragt die Datenbank ab
5. bereitet die gefundenen Daten auf
6. sendet die Antwort an das Frontend zurück

Das Frontend zeigt anschliessend die Treffer an.

</details>

<details>
<summary>📚 Mehr wissen</summary>

Das Backend kann unter anderem folgende Aufgaben übernehmen:

- Daten lesen und speichern
- fachliche Regeln ausführen
- Benutzer und Berechtigungen prüfen
- Anfragen validieren
- Berechnungen durchführen
- andere Systeme aufrufen
- Fehler behandeln
- Protokolle erstellen
- Antworten für das Frontend vorbereiten

Das Backend ist für die Benutzerin normalerweise nicht direkt sichtbar.

</details>

<details>
<summary>⚙️ Technischer Hintergrund</summary>

Ein Backend kann aus mehreren Bestandteilen bestehen:

- Server
- Anwendungslogik
- API oder Webservice
- Datenbank
- Berechtigungsprüfung
- Schnittstellen zu anderen Systemen
- Puffer oder Warteschlangen
- Cache
- Protokollierung

Die Kommunikation mit dem Frontend erfolgt häufig über HTTP oder HTTPS.

Daten werden beispielsweise als JSON oder XML übertragen.

```text
Frontend
   ↓ Anfrage
API / Webservice
   ↓
Backend
   ↓
Datenbank oder Zielsystem
   ↑
Backend erstellt Antwort
   ↑
Frontend
```

</details>

<details>
<summary>💼 Mein Arbeitsalltag</summary>

Bei einem Test kann ich Hinweise auf einen Backend-Fehler erhalten, wenn:

- korrekte Eingaben falsch verarbeitet werden
- erwartete Daten fehlen
- eine Berechtigungsprüfung fehlschlägt
- Daten nicht gespeichert werden
- ein Webservice eine unerwartete Antwort liefert
- eine Datenbankabfrage falsche Treffer zurückgibt
- eine Fehlermeldung aus der Verarbeitung kommt

Dabei kann wichtig sein zu unterscheiden:

- Ist die Eingabe im Frontend korrekt?
- Wurde die Anfrage richtig übermittelt?
- Hat das Backend die Anfrage korrekt verarbeitet?
- Sind die Daten in der Datenbank vorhanden?
- Wurde die Antwort im Frontend richtig dargestellt?

</details>

<details>
<summary>🔗 Siehe auch</summary>

- [Frontend](F.md#frontend)
- [API](A.md#api)
- [Datenbank](D.md#datenbank)
- [Webservice](W.md#webservice)
- [JSON](J.md#json)
- [XML](X.md#xml)

</details>