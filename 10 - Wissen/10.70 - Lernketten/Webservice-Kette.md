

Diese Lernkette zeigt vereinfacht, wie eine Anfrage zwischen zwei Systemen aufgebaut, übertragen, verarbeitet und beantwortet wird.

> **Merksatz:** Regeln festlegen → Anfrage senden → Daten prüfen → Verarbeitung durchführen → Antwort zurückgeben

---

## Übersicht

```text
Anfragendes System
        ↓
API legt die Regeln fest
        ↓
Anfrage wird erstellt
        ↓
Daten werden strukturiert
zum Beispiel als XML oder JSON
        ↓
Anfrage wird über das Netzwerk übertragen
        ↓
Webservice nimmt die Anfrage entgegen
        ↓
Daten und Berechtigungen werden geprüft
        ↓
Anfrage wird verarbeitet
oder an ein Zielsystem weitergeleitet
        ↓
Antwort wird erstellt
        ↓
Antwort gelangt zum anfragenden System zurück
```

Je nach Anwendung können zusätzlich ein **Puffer**, ein **Cache** oder ein **Rollbackmechanismus** eingesetzt werden.

---

<details>
<summary>1️⃣ Das anfragende System benötigt Daten oder eine Funktion</summary>

Eine Anwendung benötigt Informationen aus einem anderen System oder möchte dort eine Aktion auslösen.

Beispiele:

- SAP sucht Personendaten.
- Eine Fachanwendung übermittelt einen neuen Datensatz.
- Ein System prüft, ob eine bestimmte ID gültig ist.
- Eine Anwendung löst eine Synchronisation aus.

Das anfragende System wird auch als **Client** bezeichnet.

</details>

<details>
<summary>2️⃣ Die API legt die Kommunikationsregeln fest</summary>

Die **API** beschreibt, wie das anfragende System mit dem Webservice kommunizieren darf.

Sie legt beispielsweise fest:

- welche Anfragen möglich sind
- welche Angaben erforderlich sind
- welche Felder übermittelt werden dürfen
- welches Datenformat verwendet wird
- welche Antworten möglich sind
- welche Fehlermeldungen zurückgegeben werden

> **Merksatz:**  
> API = Regeln und Sprache der Kommunikation

</details>

<details>
<summary>3️⃣ Die Anfrage wird erstellt</summary>

Das anfragende System erstellt eine Anfrage.

Diese kann beispielsweise enthalten:

- eine Personen-ID
- einen Suchbegriff
- Filter
- Pflichtfelder
- Checkbox-Werte
- Benutzer- oder Berechtigungsinformationen
- die gewünschte Aktion

Beispiel:

```text
Aktion: Person suchen
Personen-ID: 12345
Nur prüfen: false
Daten speichern: true
```

Die Anfrage wird häufig auch als **Request** bezeichnet.

</details>

<details>
<summary>4️⃣ XML oder JSON strukturiert die Daten</summary>

Die Daten einer Anfrage können beispielsweise als **XML** oder **JSON** aufgebaut sein.

Beispiel in XML:

```xml
<Personenanfrage>
  <PersonenID>12345</PersonenID>
  <NurPruefen>false</NurPruefen>
  <DatenSpeichern>true</DatenSpeichern>
</Personenanfrage>
```

XML legt fest, welche Bedeutung die einzelnen Werte besitzen.

Es transportiert die Daten jedoch nicht selbst. Für die Übertragung wird meist ein Netzwerkprotokoll wie HTTP oder HTTPS verwendet.

> **Merksatz:**  
> XML strukturiert die Daten.  
> HTTPS überträgt die Daten.

</details>

<details>
<summary>5️⃣ Die Anfrage wird übertragen</summary>

Die Anfrage wird über ein Netzwerk an den Webservice gesendet.

Dabei können verschiedene Probleme auftreten:

- Netzwerkverbindung unterbrochen
- falsche Adresse
- Zielsystem nicht erreichbar
- Zeitüberschreitung
- Zertifikatsfehler
- Verbindung wird blockiert

Bei geschützten Verbindungen wird häufig **HTTPS** verwendet.

</details>

<details>
<summary>6️⃣ Der Webservice nimmt die Anfrage entgegen</summary>

Der **Webservice** empfängt die Anfrage und prüft zunächst, ob sie verarbeitet werden kann.

Geprüft werden können beispielsweise:

- Ist die Anfrage vollständig?
- Sind alle Pflichtfelder vorhanden?
- Ist das Datenformat korrekt?
- Ist die Benutzerin berechtigt?
- Sind Token oder Zertifikat gültig?
- Besitzen die Werte das richtige Format?
- Ist die gewünschte Aktion erlaubt?

Ist die Anfrage ungültig, sendet der Webservice eine Fehlermeldung zurück.

</details>

<details>
<summary>7️⃣ Die Anfrage wird verarbeitet</summary>

Nach erfolgreicher Prüfung verarbeitet der Webservice die Anfrage selbst oder leitet sie an ein Zielsystem weiter.

Mögliche Aktionen sind:

- Daten aus einer Datenbank lesen
- einen Datensatz erstellen
- bestehende Daten ändern
- Daten löschen
- eine fachliche Prüfung durchführen
- eine weitere Anwendung aufrufen

Vereinfacht:

```text
Anfragendes System
        ↓
Webservice
        ↓
Datenbank oder Zielsystem
```

</details>

<details>
<summary>8️⃣ Die Antwort wird erstellt und zurückgesendet</summary>

Nach der Verarbeitung erstellt der Webservice eine Antwort.

Diese kann enthalten:

- die gesuchten Daten
- eine Bestätigung
- einen Bearbeitungsstatus
- eine Warnung
- eine Fehlermeldung
- die Information, dass keine Treffer gefunden wurden

Beispiel:

```xml
<Personenantwort>
  <Status>Erfolgreich</Status>
  <PersonenID>12345</PersonenID>
  <Nachname>Muster</Nachname>
  <Vorname>Anna</Vorname>
</Personenantwort>
```

Die Antwort wird häufig als **Response** bezeichnet.

Das anfragende System wertet sie aus und zeigt das Ergebnis an oder verarbeitet es weiter.

</details>

<details>
<summary>📥 Wo kommt der Puffer ins Spiel?</summary>

Ein **Puffer** wird verwendet, wenn Daten oder Anfragen nicht sofort verarbeitet werden können.

Beispielsweise treffen sehr viele Anfragen gleichzeitig ein:

```text
Anfrage A ─┐
Anfrage B ─┼─→ Puffer → Verarbeitung
Anfrage C ─┘
```

Der Puffer hält die Anfragen kurzfristig bereit.

Er kann helfen:

- Lastspitzen auszugleichen
- Anfragen geordnet abzuarbeiten
- unterschiedliche Verarbeitungsgeschwindigkeiten auszugleichen
- Datenverluste zu verhindern

Ein Puffer ist nicht zwingend bei jedem Webservice vorhanden.

> **Merksatz:** Puffer = Daten warten auf Verarbeitung.

</details>

<details>
<summary>⚡ Wo kommt der Cache ins Spiel?</summary>

Ein **Cache** speichert häufig benötigte oder bereits geladene Daten für einen schnelleren Wiederzugriff.

Beispiel:

1. Eine Anwendung fragt eine häufig benötigte Liste ab.
2. Der Webservice lädt die Liste aus der Datenbank.
3. Eine Kopie wird im Cache gespeichert.
4. Bei der nächsten Anfrage kann die Liste direkt aus dem Cache geliefert werden.

```text
Anfrage
   ↓
Sind die Daten im Cache?
   ↙                 ↘
 Ja                   Nein
 ↓                      ↓
sofort liefern      Datenbank abfragen
                         ↓
                    Cache aktualisieren
```

Ein Cache kann die Antwortzeit verkürzen und die Datenbank entlasten.

Er muss jedoch korrekt aktualisiert werden, damit keine veralteten Daten zurückgegeben werden.

> **Merksatz:** Cache = Daten schneller wiederverwenden.

</details>

<details>
<summary>↩️ Wo kommt der Rollbackmechanismus ins Spiel?</summary>

Ein **Rollbackmechanismus** wird wichtig, wenn eine Anfrage Daten verändert und während der Verarbeitung ein Fehler auftritt.

Beispiel:

```text
Webservice startet Verarbeitung
              ↓
mehrere Daten werden geändert
              ↓
Fehler tritt auf
              ↓
Rollback wird ausgelöst
              ↓
Änderungen werden zurückgenommen
```

Dadurch wird verhindert, dass nur ein Teil der Änderungen gespeichert bleibt.

Ein Rollback ist vor allem bei folgenden Vorgängen wichtig:

- mehrere zusammengehörende Datenbankänderungen
- Datenimporte
- Buchungen
- Synchronisationen
- Updates

Bei einer reinen Suchanfrage ohne Datenänderung ist normalerweise kein Rollback erforderlich.

> **Merksatz:** Rollback = fehlerhafte Änderungen zurücknehmen.

</details>

<details>
<summary>⚠️ Wo können Fehler auftreten?</summary>

### API oder Anfrage

- falsche Aktion verwendet
- Pflichtfeld fehlt
- ungültiger Parameter
- falsche Checkbox gesetzt

### XML oder Datenformat

- falsche Struktur
- Tag fehlt
- ungültiger Wert
- falscher Datentyp

### Netzwerk

- Webservice nicht erreichbar
- Verbindung unterbrochen
- Timeout
- falsche Adresse

### Berechtigungen

- Benutzer nicht berechtigt
- Token ungültig oder abgelaufen
- Zertifikat wird nicht akzeptiert
- benötigte Rolle fehlt

### Webservice

- Fehler in der Verarbeitung
- falsche Konfiguration
- Dienst nicht verfügbar
- unerwarteter Programmfehler

### Zielsystem oder Datenbank

- benötigte Daten fehlen
- Datenbank nicht erreichbar
- fachliche Regel verhindert die Verarbeitung
- Zielsystem liefert einen Fehler

### Puffer

- Puffer ist voll
- Anfrage bleibt hängen
- Reihenfolge ist falsch
- Daten gehen verloren

### Cache

- veraltete Daten
- Cache wurde nicht aktualisiert
- falscher Cache-Eintrag wird verwendet

### Rollback

- Änderungen werden nur teilweise zurückgenommen
- ursprünglicher Zustand wird nicht vollständig hergestellt
- Rollback wird nicht ausgelöst

</details>

<details>
<summary>💼 Mein Arbeitsalltag</summary>

Bei einem Webservice-Test kann ich den Ablauf Schritt für Schritt prüfen:

1. Welche Anfrage wurde ausgelöst?
2. Entspricht sie den Regeln der API?
3. Sind alle Pflichtfelder vorhanden?
4. Sind Checkboxen und Parameter korrekt?
5. Ist das XML richtig aufgebaut?
6. Wurde die Anfrage erfolgreich übertragen?
7. Besitzt die Benutzerin die benötigte Berechtigung?
8. Hat der Webservice die Anfrage verarbeitet?
9. Wurde das Zielsystem erreicht?
10. Ist die Antwort vollständig und korrekt?
11. Wird die Antwort in SAP richtig angezeigt?
12. Werden Fehler verständlich zurückgemeldet?
13. Wurden bei einem Fehler Änderungen zurückgesetzt?

Wichtig ist, nicht automatisch davon auszugehen, dass ein gemeldeter Webservice-Fehler tatsächlich im Webservice entstanden ist.

Die Ursache kann auch bei den Daten, der Berechtigung, dem Netzwerk oder im Zielsystem liegen.

</details>

<details>
<summary>🧠 Gesamtmerksatz</summary>

```text
API
↓
legt die Regeln fest

XML oder JSON
↓
strukturiert die Daten

HTTPS
↓
überträgt die Anfrage

Webservice
↓
prüft und verarbeitet die Anfrage

Zielsystem
↓
liefert oder verändert Daten

Webservice
↓
sendet die Antwort zurück
```

Optional:

```text
Puffer
= Anfragen warten auf Verarbeitung

Cache
= häufig benötigte Daten schneller liefern

Rollback
= Änderungen bei einem Fehler zurücknehmen
```

</details>

<details>
<summary>🔗 Beteiligte Glossarbegriffe</summary>

- [API](<../10.10 - Glossar/A.md#api>)
- [Cache](<../10.10 - Glossar/C.md#cache>)
- [Puffer](<../10.10 - Glossar/P.md#puffer>)
- [Rollbackmechanismus](<../10.10 - Glossar/R.md#rollbackmechanismus>)
- [Webservice](<../10.10 - Glossar/W.md#webservice>)
- [XML](<../10.10 - Glossar/X.md#xml>)

</details>

<details>
<summary>📖 Passende Vertiefungsseiten</summary>

- [API – ausführliche Erklärung](<../10.60 - Vertiefungsseiten/API.md>)
- [Puffer – ausführliche Erklärung](<../10.60 - Vertiefungsseiten/Puffer.md>)
- [Rollbackmechanismus – ausführliche Erklärung](<../10.60 - Vertiefungsseiten/Rollbackmechanismus.md>)
- [Webservice – ausführliche Erklärung](<../10.60 - Vertiefungsseiten/Webservice.md>)

</details>