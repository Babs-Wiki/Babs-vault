
# Windows – Ereignisanzeige (Event Viewer)

Die **Windows-Ereignisanzeige** zeigt protokollierte Ereignisse von Windows, Programmen, Diensten und Sicherheitsfunktionen.

> **Merksatz:** Die Ereignisanzeige hilft herauszufinden, was auf einem Computer zu einem bestimmten Zeitpunkt passiert ist.

---

<details>
<summary>📖 Was ist die Ereignisanzeige?</summary>

Die Ereignisanzeige ist ein in Windows enthaltenes Werkzeug zur Anzeige von sogenannten **Ereignisprotokollen**.

Darin können unter anderem protokolliert werden:

- Programmfehler
- Windows-Fehler
- Warnungen
- Start- und Herunterfahrvorgänge
- Anmeldeversuche
- Probleme mit Diensten
- Installationen und Updates
- sicherheitsrelevante Ereignisse

Die Ereignisanzeige ist besonders bei der Fehlersuche hilfreich.

Sie zeigt jedoch nur Ereignisse, die tatsächlich protokolliert wurden und für welche die nötigen Berechtigungen vorhanden sind.

</details>

<details>
<summary>▶️ Ereignisanzeige starten</summary>

### Über die Windows-Suche

```text
Windows-Taste drücken
        ↓
Ereignisanzeige eingeben
        ↓
Ereignisanzeige öffnen
```

### Über den Ausführen-Dialog

```text
Win + R
```

Danach eingeben:

```text
eventvwr.msc
```

Anschliessend mit `Enter` bestätigen.

</details>

<details>
<summary>🗂️ Wichtige Bereiche</summary>

Unter **Windows-Protokolle** befinden sich verschiedene Kategorien.

| Bereich | Inhalt |
|---|---|
| **Anwendung** | Meldungen und Fehler von installierten Programmen |
| **Sicherheit** | Anmeldungen, Zugriffe und sicherheitsrelevante Ereignisse |
| **Installation** | Ereignisse zu Installationen und Windows-Komponenten |
| **System** | Meldungen von Windows, Treibern, Diensten und Hardware |
| **Weitergeleitete Ereignisse** | Ereignisse, die von anderen Computern übertragen wurden |

Zusätzlich gibt es:

- benutzerdefinierte Ansichten
- Anwendungs- und Dienstprotokolle
- Protokolle einzelner Windows-Komponenten

</details>

<details>
<summary>🚦 Ereignisstufen</summary>

Ereignisse können unterschiedliche Stufen besitzen.

| Stufe | Bedeutung |
|---|---|
| **Information** | Ein Vorgang wurde ausgeführt oder dokumentiert |
| **Warnung** | Es besteht ein mögliches Problem |
| **Fehler** | Ein Vorgang ist fehlgeschlagen oder wurde beeinträchtigt |
| **Kritisch** | Es ist ein schwerwiegendes Problem aufgetreten |
| **Überwachung erfolgreich** | Ein überwachter Sicherheitsvorgang war erfolgreich |
| **Überwachung fehlgeschlagen** | Ein überwachter Sicherheitsvorgang ist fehlgeschlagen |

Nicht jede Warnung bedeutet automatisch, dass ein akutes Problem besteht.

Wichtig sind immer der Zeitpunkt, die Quelle und der Zusammenhang mit dem beobachteten Fehler.

</details>

<details>
<summary>🔍 Informationen eines Ereignisses</summary>

Ein Ereignis enthält normalerweise mehrere Angaben.

| Information | Bedeutung |
|---|---|
| **Datum und Uhrzeit** | Zeitpunkt des Ereignisses |
| **Quelle** | Programm, Dienst oder Windows-Komponente |
| **Ereignis-ID** | Nummer zur Kennzeichnung des Ereignistyps |
| **Stufe** | Information, Warnung, Fehler oder kritisch |
| **Benutzer** | Betroffenes Benutzerkonto, sofern vorhanden |
| **Computer** | Computer, auf dem das Ereignis protokolliert wurde |
| **Allgemein** | Lesbare Beschreibung des Ereignisses |
| **Details** | Zusätzliche technische Informationen |

Die **Ereignis-ID** allein reicht häufig nicht aus. Auch die Quelle und die Beschreibung müssen berücksichtigt werden.

</details>

<details>
<summary>🔎 In Ereignissen suchen und filtern</summary>

Bei vielen Einträgen ist es sinnvoll, die Anzeige einzugrenzen.

### Aktuelles Protokoll filtern

Im rechten Bereich kann **Aktuelles Protokoll filtern** gewählt werden.

Gefiltert werden kann beispielsweise nach:

- Zeitraum
- Ereignisstufe
- Ereignisquelle
- Ereignis-ID
- Benutzer
- Schlüsselwörtern

### Suchen

Mit der Funktion **Suchen** kann innerhalb eines geöffneten Protokolls nach einem Begriff gesucht werden.

Mögliche Suchbegriffe sind beispielsweise:

- Name eines Programms
- Dienstname
- Fehlertext
- Ereignis-ID
- Benutzername

</details>

<details>
<summary>🧭 Vorgehen bei einer Fehleranalyse</summary>

Ein mögliches Vorgehen:

1. Zeitpunkt des Problems möglichst genau notieren.
2. Ereignisanzeige öffnen.
3. Zuerst **Windows-Protokolle → Anwendung** prüfen.
4. Danach bei Bedarf **Windows-Protokolle → System** prüfen.
5. Ereignisse auf den passenden Zeitraum eingrenzen.
6. Nach Warnungen, Fehlern oder kritischen Ereignissen suchen.
7. Quelle, Ereignis-ID und Beschreibung kontrollieren.
8. Prüfen, ob das Ereignis zeitlich und inhaltlich zum Problem passt.
9. Relevante Informationen dokumentieren.
10. Erst danach eine mögliche Massnahme ableiten.

> **Wichtig:** Nicht jeder gleichzeitig auftretende Fehler ist automatisch die Ursache des beobachteten Problems.

</details>

<details>
<summary>💡 Beispiel</summary>

Eine Anwendung stürzt um ungefähr `10:15 Uhr` ab.

Vorgehen:

```text
Zeitpunkt notieren
      ↓
Ereignisanzeige öffnen
      ↓
Windows-Protokolle → Anwendung
      ↓
Zeitraum um 10:15 Uhr prüfen
      ↓
Fehler der betroffenen Anwendung öffnen
      ↓
Quelle, Ereignis-ID und Beschreibung kontrollieren
```

Möglicherweise enthält das Ereignis Hinweise auf:

- das abgestürzte Programm
- ein fehlerhaftes Modul
- einen Berechtigungsfehler
- eine nicht erreichbare Datei
- einen Fehler in einer Windows-Komponente

</details>

<details>
<summary>🔐 Anmeldungen und Benutzerereignisse</summary>

Im Sicherheitsprotokoll können je nach Konfiguration und Berechtigung unter anderem Anmeldeereignisse protokolliert werden.

Damit kann beispielsweise geprüft werden:

- ob eine Anmeldung erfolgreich war
- ob eine Anmeldung fehlgeschlagen ist
- wann sich ein Benutzer angemeldet hat
- welches Benutzerkonto betroffen war
- ob ein Zugriff verweigert wurde

Die Ereignisanzeige ist jedoch kein vollständiges Überwachungsprotokoll sämtlicher Benutzeraktivitäten.

Welche Ereignisse vorhanden sind, hängt unter anderem von den aktivierten Überwachungsrichtlinien ab.

</details>

<details>
<summary>⚙️ Technischer Hintergrund</summary>

Windows und installierte Programme schreiben Ereignisse in verschiedene Protokolldateien.

Ein Ereignis wird normalerweise von einer bestimmten **Quelle** erzeugt.

Beispiele für Quellen:

- ein Windows-Dienst
- ein Gerätetreiber
- eine Anwendung
- eine Sicherheitskomponente
- eine Update-Funktion

Protokolle besitzen eine begrenzte Grösse.

Ist ein Protokoll voll, können je nach Einstellung:

- ältere Ereignisse überschrieben werden
- neue Ereignisse nicht mehr gespeichert werden
- Ereignisse archiviert werden

Darum sind sehr alte Ereignisse möglicherweise nicht mehr vorhanden.

</details>

<details>
<summary>💼 Mein Arbeitsalltag</summary>

Die Ereignisanzeige kann mir bei der Fehlersuche helfen, wenn:

- ein Programm abstürzt
- ein Dienst nicht startet
- ein Computer unerwartet herunterfährt
- eine Anmeldung fehlschlägt
- eine Installation nicht funktioniert
- eine Anwendung keine Verbindung herstellen kann
- eine Fehlermeldung keine ausreichenden Informationen enthält

Bei der Prüfung achte ich besonders auf:

- den genauen Zeitpunkt
- die Ereignisquelle
- die Ereignis-ID
- die Beschreibung
- betroffene Benutzer oder Programme
- gleichzeitig aufgetretene Ereignisse

Relevante technische Angaben kann ich für ein Ticket oder eine Rückfrage an die Entwicklung dokumentieren, sofern sie keine vertraulichen Inhalte enthalten.

</details>

<details>
<summary>⚠️ Wichtige Hinweise</summary>

- Nicht jede Warnung muss behoben werden.
- Nicht jeder Fehler ist die Ursache des aktuellen Problems.
- Sicherheitsprotokolle können besondere Berechtigungen erfordern.
- Ereignisse sollten nicht ohne Grund gelöscht werden.
- Vor Änderungen an Protokolleinstellungen muss deren Auswirkung bekannt sein.
- Vertrauliche Informationen gehören nicht ins private Wiki.
- Ereignisbeschreibungen können technische oder personenbezogene Angaben enthalten.

</details>

<details>
<summary>🔗 Siehe auch</summary>

- [Ereignisanzeige im Glossar](<../10.10 - Begriffe und Definitionen/E.md#ereignisanzeige-event-viewer>)
- [Windows – Kurzbefehle & Befehle](<Windows – Kurzbefehle & Befehle.md>)

</details>