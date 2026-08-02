- [Performant und inperformant](#performant-und-inperformant)
- [Plain Text](#plain-text)
- [POC](#poc)
- [Primärschlüssel](#primärschlüssel)
- [Proxy](#proxy)
- [Puffer](#puffer)

### POC

| Begriff | Deutsch | Merksatz |
|----------|---------|----------|
| **Proof of Concept (POC)** | Machbarkeitsnachweis | **Ein POC zeigt, ob eine Idee technisch grundsätzlich funktionieren kann.** |

Ein Proof of Concept ist ein kleiner Versuch oder Prototyp, mit dem die Machbarkeit einer technischen Idee geprüft wird.

<details>
<summary>💡 Beispiel</summary>

Bevor eine neue Schnittstelle vollständig entwickelt wird, erstellt das Team einen kleinen POC.

Damit wird getestet, ob zwei Systeme überhaupt wie geplant Daten austauschen können.

</details>

<details>
<summary>📚 Mehr Wissen</summary>

Ein POC ist noch kein fertiges Produkt. Er dient dazu, technische Risiken frühzeitig zu erkennen, bevor viel Zeit und Geld investiert wird.

</details>

<details>
<summary>⚙️ Technik</summary>

Bei einem POC werden meistens nur die wichtigsten Funktionen umgesetzt.

Design, Benutzerfreundlichkeit, vollständige Fehlerbehandlung und Sicherheit stehen dabei oft noch nicht im Vordergrund.

</details>

### Performant und inperformant

| Begriff | Deutsch | Merksatz |
|----------|---------|----------|
| **Performant / inperformant** | Leistungsfähig und effizient / langsam oder ineffizient | **Performant bedeutet: Eine Anwendung erledigt ihre Arbeit schnell und ressourcenschonend.** |

**Performant** bedeutet, dass ein Programm, eine Abfrage oder ein System schnell und effizient arbeitet.

**Inperformant** bedeutet, dass unnötig viel Zeit, Arbeitsspeicher oder Rechenleistung benötigt wird.

<details>
<summary>💡 Beispiel</summary>

Eine Datenbankabfrage benötigt weniger als eine Sekunde und belastet das System kaum:

**Performant**

Die gleiche Abfrage benötigt dreissig Sekunden und durchsucht unnötig sämtliche Datensätze:

**Inperformant**

</details>

<details>
<summary>📚 Mehr Wissen</summary>

Die Performance kann unter anderem beeinflusst werden durch:

- langsame Datenbankabfragen
- unnötig grosse Datenmengen
- schlechte Programmierung
- fehlende Zwischenspeicherung
- zu wenig Arbeitsspeicher oder Rechenleistung

Der Begriff **inperformant** wird in der Informatik häufig verwendet. Sprachlich ist auch **nicht performant** üblich.

</details>

<details>
<summary>⚙️ Technik</summary>

Die Leistung eines Systems wird beispielsweise anhand folgender Werte beurteilt:

- Antwortzeit
- Verarbeitungsdauer
- Speicherverbrauch
- CPU-Auslastung
- Anzahl verarbeiteter Anfragen

Eine Optimierung dieser Werte wird als **Performance-Optimierung** bezeichnet.

</details>

### Proxy

| Begriff | Deutsch | Merksatz |
|----------|---------|----------|
| **Proxy** | Vermittler zwischen Benutzer und Server | **Ein Proxy nimmt Anfragen entgegen und leitet sie an ein anderes System weiter.** |

Ein Proxy ist ein zwischengeschaltetes System, das Anfragen zwischen einem Client und einem Server vermittelt.

<details>
<summary>💡 Beispiel</summary>

Ein Computer ruft eine Webseite nicht direkt auf.

Die Anfrage wird zuerst an den Proxy gesendet. Dieser prüft die Anfrage und leitet sie anschliessend an den Webserver weiter.

Die Antwort gelangt ebenfalls über den Proxy zurück.

</details>

<details>
<summary>📚 Mehr Wissen</summary>

Ein Proxy kann verschiedene Aufgaben übernehmen:

- Zugriffe kontrollieren
- unerlaubte Webseiten sperren
- Anfragen protokollieren
- Inhalte zwischenspeichern
- interne Systeme schützen
- die Identität des Clients gegenüber dem Zielserver verbergen

</details>

<details>
<summary>⚙️ Technik</summary>

Ein **Forward Proxy** steht auf der Seite des Clients und vermittelt dessen Anfragen an externe Server.

Ein **Reverse Proxy** steht vor einem oder mehreren Servern und nimmt Anfragen der Clients entgegen.

Ein Reverse Proxy kann unter anderem:

- Anfragen auf mehrere Server verteilen
- HTTPS-Verbindungen verwalten
- interne Server verbergen
- häufig benötigte Inhalte zwischenspeichern

</details>

### Plain Text

| Begriff | Deutsch | Merksatz |
|----------|---------|----------|
| **Plain Text** | Reiner, unformatierter Text | **Plain Text enthält Zeichen und Inhalt, aber keine sichtbare Gestaltung.** |

Plain Text ist reiner Text ohne Formatierungen wie Schriftart, Schriftgrösse, Farbe, Bilder oder Seitenlayout.

<details>
<summary>💡 Beispiel</summary>

Eine `.txt`-Datei enthält normalerweise Plain Text.

Auch Markdown-Dateien bestehen grundsätzlich aus Plain Text. Die Formatierung wird durch Zeichen wie `#`, `**` oder `-` beschrieben und erst bei der Darstellung sichtbar.

</details>

<details>
<summary>📚 Mehr Wissen</summary>

Plain Text kann mit einfachen Texteditoren geöffnet werden.

Typische Plain-Text-Dateien sind:

- `.txt`
- `.md`
- `.csv`
- `.json`
- `.xml`
- Programmcode

Ein Word-Dokument ist dagegen keine reine Plain-Text-Datei, weil es zusätzliche Formatierungs- und Layoutinformationen enthält.

</details>

<details>
<summary>⚙️ Technik</summary>

Plain Text wird mit einer Zeichenkodierung gespeichert.

Eine häufig verwendete Zeichenkodierung ist **UTF-8**. Sie ermöglicht die Darstellung vieler verschiedener Zeichen und Sprachen.

Wird eine Datei mit der falschen Zeichenkodierung geöffnet, können Umlaute oder Sonderzeichen falsch dargestellt werden.

</details>

### Puffer

| Bereich | Inhalt |
|---|---|
| 🇬🇧 Englisch | Buffer |
| 🇩🇪 Deutsch | Puffer / Zwischenspeicher |
| 🎯 Wozu dient das? | Ein Puffer nimmt Daten vorübergehend auf, bis sie weiterverarbeitet werden können. Er gleicht unterschiedliche Verarbeitungsgeschwindigkeiten aus und verhindert, dass Daten verloren gehen. |
| 🧠 Merksatz | **Ein Puffer ist ein Wartebereich für Daten.** |

<details>
<summary>💡 Beispiel</summary>

Mehrere Personen senden gleichzeitig einen Druckauftrag.

Die Aufträge werden in einer Druckerwarteschlange zwischengespeichert und anschliessend nacheinander verarbeitet.

```text
Druckaufträge
      ↓
    Puffer
      ↓
    Drucker
```

</details>

<details>
<summary>📚 Mehr wissen</summary>

Ein Puffer wird eingesetzt, wenn Daten schneller eintreffen, als sie verarbeitet werden können.

Typische Beispiele sind:

- Druckaufträge
- Webservice-Anfragen
- Datenimporte
- Log-Daten
- Audio- und Videodaten

Ein Puffer speichert Daten nur vorübergehend. Nach ihrer Verarbeitung werden sie normalerweise wieder entfernt.

</details>

<details>
<summary>⚙️ Technischer Hintergrund</summary>

Ein Puffer kann sich beispielsweise im Arbeitsspeicher, in einer Datei oder in einer Warteschlange befinden.

Die Daten können:

- in der Reihenfolge ihres Eingangs
- nach einer festgelegten Priorität
- durch mehrere parallele Prozesse

verarbeitet werden.

Ist ein Puffer voll, muss das System festlegen, ob es neue Daten ablehnt, wartet oder zusätzlichen Speicher verwendet.

</details>

<details>
<summary>🔗 Siehe auch</summary>

- [Cache](C.md#cache)
- [Synchron und asynchron](S.md#synchron-und-asynchron)
- [[Webservice|websevice]]

</details>

<details>
<summary>📖 Vertiefung</summary>

- [Puffer – ausführliche Erklärung](<../10.60 - Vertiefungsseiten/Puffer.md>)

</details>

## Primärschlüssel

| Feld | Inhalt |
|------|--------|
| 🇬🇧 **Englisch** | Primary Key |
| 🇩🇪 **Deutsch** | Primärschlüssel |
| 🎯 **Wozu dient das?** | Ein Primärschlüssel kennzeichnet jeden Datensatz in einer Datenbanktabelle eindeutig. Dadurch kann ein Datensatz zuverlässig gefunden und von allen anderen unterschieden werden. |
| 🧠 **Merksatz** | **Der Primärschlüssel ist die eindeutige Identitätsnummer eines Datensatzes.** |

<details>
<summary>💡 Beispiel</summary>

In einer Tabelle mit Personen könnten mehrere Personen gleich heissen.

Darum erhält jede Person eine eindeutige Nummer:

| Personen-ID | Name |
|---|---|
| 1001 | Anna Müller |
| 1002 | Anna Müller |

Die **Personen-ID** ist der Primärschlüssel. Obwohl beide Personen gleich heissen, können ihre Datensätze eindeutig unterschieden werden.

</details>

<details>
<summary>📚 Mehr wissen</summary>

Ein Primärschlüssel:

- darf innerhalb einer Tabelle nicht doppelt vorkommen,
- darf normalerweise nicht leer sein,
- sollte sich möglichst nicht verändern.

Häufig wird dafür eine automatisch vergebene ID verwendet.

</details>

<details>
<summary>⚙️ Technischer Hintergrund</summary>

Ein Primärschlüssel besteht meistens aus einer einzelnen Spalte, zum Beispiel `Personen-ID`.

Er kann aber auch aus mehreren Spalten zusammengesetzt sein. Das nennt man einen **zusammengesetzten Primärschlüssel**.

Andere Tabellen können über einen Fremdschlüssel auf diesen Primärschlüssel verweisen. Dadurch entstehen Beziehungen zwischen Tabellen.

</details>

<details>
<summary>💼 Mein Arbeitsalltag</summary>

Bei Tests oder Fehlersuchen können eindeutige IDs helfen, genau den richtigen Datensatz zu finden – zum Beispiel eine bestimmte Person, ein Ereignis, ein Dokument oder einen Vorgang.

</details>

<details>
<summary>🔗 Siehe auch</summary>

- [[D#Datenbank|Datenbank]]

</details>