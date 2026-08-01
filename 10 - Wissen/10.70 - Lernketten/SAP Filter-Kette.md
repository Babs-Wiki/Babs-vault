
Diese Lernkette zeigt vereinfacht, wie eine Eingabe in SAP zu einer Datenbankabfrage führt und wie die gefundenen Werte wieder zur Benutzeroberfläche zurückgelangen.

> **Merksatz:** Eingabe → Anfrage → Datenbankabfrage → Treffer → Aufbereitung → Anzeige

---

## Übersicht

```text
Benutzerin gibt einen Suchwert ein
                 ↓
Smart Value Help startet die Suche
                 ↓
Suchanfrage wird an das System gesendet
                 ↓
Query fragt passende Daten ab
                 ↓
Datenbank sucht nach Treffern
                 ↓
Gefundene Daten werden zurückgegeben
                 ↓
Mapping ordnet die Daten den richtigen Feldern zu
                 ↓
Daten werden bei Bedarf als XML übertragen
                 ↓
Webservice liefert die Antwort an SAP zurück
                 ↓
Smart Value Help zeigt die Treffer an
```

---

<details>
<summary>1️⃣ Eingabe in SAP</summary>

Die Benutzerin gibt in einem SAP-Feld einen Suchwert ein, beispielsweise:

```text
Ort: Thun
```

Je nach Eingabe können bereits während des Tippens passende Vorschläge gesucht werden.

</details>

<details>
<summary>2️⃣ Smart Value Help startet die Suche</summary>

Die **Smart Value Help** ist eine intelligente Such- und Auswahlhilfe.

Sie übernimmt die Eingabe und löst eine Anfrage aus, damit passende und gültige Werte gesucht werden können.

Beispielsweise:

```text
Eingabe: Thu
Gesuchte Werte: Orte, die mit „Thu“ beginnen
```

</details>

<details>
<summary>3️⃣ Die Anfrage wird weitergeleitet</summary>

Die Suchanfrage wird an den zuständigen Dienst beziehungsweise Webservice weitergeleitet.

Dabei können zusätzliche Angaben mitgesendet werden, beispielsweise:

- eingegebener Suchtext
- ausgewähltes Land
- Benutzerberechtigung
- gewünschte Anzahl Treffer
- weitere Filter

</details>

<details>
<summary>4️⃣ Query erstellt die Datenbankabfrage</summary>

Eine **Query** ist eine Abfrage an eine Datenbank.

Sie beschreibt, welche Daten gesucht werden sollen.

Vereinfacht könnte die Abfrage lauten:

```sql
SELECT Ort
FROM Ortschaften
WHERE Ort LIKE 'Thu%';
```

Die Query sucht in diesem Beispiel nach Orten, die mit `Thu` beginnen.

Die genaue Abfrage wird normalerweise im Hintergrund durch die Anwendung oder den zuständigen Dienst erstellt.

</details>

<details>
<summary>5️⃣ Datenbank sucht die Treffer</summary>

Die Datenbank durchsucht die gespeicherten Daten nach passenden Einträgen.

Mögliche Treffer sind beispielsweise:

```text
Thun
Thunstetten
Thurnen
```

Die gefundenen Datensätze werden an die aufrufende Anwendung zurückgegeben.

</details>

<details>
<summary>6️⃣ Mapping ordnet die Daten zu</summary>

Beim **Mapping** werden Daten aus einer Struktur den passenden Feldern einer anderen Struktur zugeordnet.

Beispielsweise:

| Datenbankfeld | Feld in der Antwort |
|---|---|
| `ORT_NAME` | `Ortsname` |
| `PLZ_NR` | `Postleitzahl` |
| `LAND_CODE` | `Land` |

Das Mapping sorgt dafür, dass jedes empfangende System weiss, welcher Wert in welches Feld gehört.

</details>

<details>
<summary>7️⃣ Daten werden bei Bedarf als XML übertragen</summary>

Je nach eingesetzter Schnittstelle können die Daten als XML verpackt und übertragen werden.

Beispiel:

```xml
<Ortschaft>
  <Ortsname>Thun</Ortsname>
  <Postleitzahl>3600</Postleitzahl>
  <Land>CH</Land>
</Ortschaft>
```

XML ist jedoch nicht bei jeder Schnittstelle zwingend. Manche Systeme verwenden beispielsweise JSON oder ein anderes Datenformat.

</details>

<details>
<summary>8️⃣ Webservice liefert die Antwort zurück</summary>

Der Webservice sendet die gefundenen und aufbereiteten Daten zurück an SAP.

Dabei kann die Antwort enthalten:

- gefundene Treffer
- zusätzliche Beschreibungen
- technische Statusinformationen
- eine Fehlermeldung
- die Meldung, dass keine Treffer gefunden wurden

</details>

<details>
<summary>9️⃣ Smart Value Help zeigt die Treffer an</summary>

SAP verarbeitet die Antwort und zeigt die passenden Werte in der Smart Value Help an.

Die Benutzerin kann anschliessend einen gültigen Wert auswählen.

```text
Eingabe: Thu
        ↓
Treffer:
- Thun
- Thunstetten
- Thurnen
```

</details>

<details>
<summary>⚠️ Wo können Fehler auftreten?</summary>

### Eingabe oder Filter

- Suchwert ist falsch geschrieben
- Filter sind zu streng
- benötigte Angaben fehlen

### Query

- Abfrage sucht im falschen Feld
- Filterbedingung ist falsch
- Abfrage liefert zu viele oder keine Treffer

### Datenbank

- Datensatz fehlt
- Daten sind veraltet
- Datenbank ist nicht erreichbar

### Mapping

- Felder sind falsch zugeordnet
- ein Pflichtfeld fehlt
- Datentypen passen nicht zusammen

### XML oder Datenformat

- Struktur ist fehlerhaft
- Tag fehlt
- Wert besitzt das falsche Format

### Webservice

- Dienst ist nicht erreichbar
- Berechtigung fehlt
- Zeitüberschreitung tritt auf
- Zielsystem meldet einen Fehler

### Anzeige in SAP

- Antwort wird nicht korrekt verarbeitet
- Treffer werden falsch dargestellt
- Smart Value Help zeigt keine Werte an

</details>

<details>
<summary>💼 Mein Arbeitsalltag</summary>

Bei einem Test kann ich die Filter-Kette Schritt für Schritt prüfen:

1. Welche Eingabe wurde in SAP gemacht?
2. Welche Filter oder Parameter wurden übermittelt?
3. Wurde die Anfrage ausgelöst?
4. Liefert die Query die erwarteten Treffer?
5. Sind die benötigten Daten in der Datenbank vorhanden?
6. Sind die Felder im Mapping richtig zugeordnet?
7. Ist die übermittelte Datenstruktur korrekt?
8. Liefert der Webservice eine Antwort?
9. Werden die Treffer in SAP richtig angezeigt?

Dadurch lässt sich besser eingrenzen, an welcher Stelle ein Fehler entstanden ist.

</details>

<details>
<summary>🔗 Beteiligte Glossarbegriffe</summary>

- [Datenbank](../10.10%20-%20Glossar/D.md#datenbank)
- [Mapping](../10.10%20-%20Glossar/M.md#mapping)
- [Query](../10.10%20-%20Glossar/Q.md#query)
- [Smart Value Help](../10.10%20-%20Glossar/S.md#smart-value-help)
- [Webservice](../10.10%20-%20Glossar/W.md#webservice)
- [XML](../10.10%20-%20Glossar/X.md#xml)

</details>