- [Datenbank](#datenbank)
- [Datenformat](#datenformat)
- [Delta Load und Full Load](#delta-load-und-full-load)
- [DOM](#dom)

### Delta Load und Full Load

| Bereich | Inhalt |
|---|---|
| 🇬🇧 Englisch | Delta Load / Full Load |
| 🇩🇪 Deutsch | Änderungsladung / vollständige Datenladung |
| 🎯 Wozu dient das? | Beim Delta Load werden nur neue oder geänderte Daten übertragen. Beim Full Load wird der gesamte Datenbestand neu geladen. |
| 🧠 Merksatz | **Delta Load = nur Änderungen. Full Load = alles neu laden.** |

<details>
<summary>💡 Beispiel</summary>

In einem System befinden sich 100'000 Personendatensätze.

Seit der letzten Übertragung wurden 500 Datensätze geändert.

**Delta Load:**

Es werden nur die 500 neuen oder geänderten Datensätze übertragen.

**Full Load:**

Alle 100'000 Datensätze werden erneut übertragen.

</details>

<details>
<summary>📚 Mehr wissen</summary>

Ein Delta Load bietet häufig folgende Vorteile:

- schnellere Verarbeitung
- weniger Datenverkehr
- geringere Belastung der beteiligten Systeme
- kürzere Ladezeiten

Ein Full Load ist sinnvoll, wenn der gesamte Datenbestand neu aufgebaut oder vollständig abgeglichen werden muss.

</details>

<details>
<summary>⚙️ Technischer Hintergrund</summary>

Damit ein Delta Load funktioniert, muss das System erkennen können, welche Daten seit der letzten Übertragung:

- neu erstellt
- geändert
- oder gelöscht wurden

Dafür können beispielsweise ein Änderungsdatum, eine Versionsnummer oder ein Änderungskennzeichen verwendet werden.

Geht eine Änderung verloren oder ist der Datenbestand nicht mehr konsistent, kann ein Full Load notwendig werden.

</details>

<details>
<summary>💼 Mein Arbeitsalltag</summary>

Bei Tests kann wichtig sein zu prüfen:

- Werden tatsächlich nur geänderte Daten übertragen?
- Werden neue Datensätze erkannt?
- Werden Löschungen korrekt berücksichtigt?
- Entspricht der Datenbestand nach dem Laden dem Zielsystem?
- Funktioniert bei Bedarf auch ein vollständiger Full Load?

</details>

### Datenbank

| Feld | Inhalt |
|------|--------|
| 🇬🇧 **Englisch** | Database |
| 🇩🇪 **Deutsch** | Datenbank |
| 🎯 **Wozu dient das?** | Eine Datenbank speichert, organisiert und verwaltet Daten, damit Programme sie schnell finden, ändern und auswerten können. |
| 🧠 **Merksatz** | **Eine Datenbank ist wie ein gut organisierter Aktenschrank – nur digital.** |

<details>
<summary>💡 Beispiel</summary>

Im Polizeialltag werden Personendaten, Fahrzeuge, Ereignisse oder Dokumente in einer Datenbank gespeichert. Programme wie ICM lesen diese Daten aus oder schreiben neue Informationen hinein.

</details>

<details>
<summary>📚 Mehr wissen</summary>

Die häufigste Art ist die **relationale Datenbank**. Dort werden Informationen in Tabellen gespeichert, die miteinander verknüpft sind.

Beispiele für Datenbanksysteme sind:
- PostgreSQL
- MariaDB
- Microsoft SQL Server
- Oracle Database

</details>

<details>
<summary>⚙️ Technischer Hintergrund</summary>

Programme greifen normalerweise nicht direkt auf die Daten zu, sondern über SQL-Abfragen, APIs oder Webservices. Dadurch können Daten gesucht, eingefügt, geändert oder gelöscht werden.

</details>

<details>
<summary>💼 Mein Arbeitsalltag</summary>

Viele Anwendungen bei der Kantonspolizei arbeiten mit Datenbanken im Hintergrund. Als Informatikbetreuerin begegne ich Datenbanken beispielsweise bei Tests, Fehlersuchen oder wenn Daten über Webservices und APIs zwischen Systemen ausgetauscht werden.

</details>

<details>
<summary>🔗 Siehe auch</summary>

- [API](a.md#API)
- [[B#Backend|Backend]]
- [[D#Delta Load|Delta Load]]
- [[F#Full Load|Full Load]]
- [[Webservice|Webservice]]

</details>

<details>
<summary>📖 Vertiefung</summary>

➡️ *Folgt später: Datenbanken*

</details>

## Datenformat

| Feld | Inhalt |
|------|--------|
| 🇬🇧 **Englisch** | Data Format |
| 🇩🇪 **Deutsch** | Datenformat |
| 🎯 **Wozu dient das?** | Ein Datenformat legt fest, wie Daten aufgebaut, geschrieben, gespeichert oder zwischen Systemen übertragen werden. |
| 🧠 **Merksatz** | **Das Datenformat ist die gemeinsame Schreibweise, damit Systeme dieselben Daten verstehen.** |

<details>
<summary>💡 Beispiel</summary>

Eine Person kann beispielsweise in einem XML-Datenformat so dargestellt werden:

```xml
<person>
  <name>Muster</name>
  <vorname>Anna</vorname>
</person>
```

Die festgelegte Struktur zeigt den Systemen, welches Feld den Namen und welches den Vornamen enthält.

</details>

<details>
<summary>📚 Mehr wissen</summary>

Häufige Datenformate sind:

- **XML**
- **JSON**
- **CSV**

Dasselbe Datenformat kann von verschiedenen Programmen gelesen und verarbeitet werden.

</details>

<details>
<summary>⚙️ Technischer Hintergrund</summary>

Ein Datenformat bestimmt beispielsweise:

- die Struktur der Daten,
- die Bezeichnung der Felder,
- die erlaubten Werte,
- die Schreibweise von Datum und Uhrzeit,
- wie einzelne Datensätze voneinander getrennt werden.

Wenn Sender und Empfänger unterschiedliche Formate erwarten, kann die Übertragung fehlschlagen oder Daten können falsch interpretiert werden.

</details>

<details>
<summary>💼 Mein Arbeitsalltag</summary>

Bei Schnittstellen- und Webservice-Tests kann ich kontrollieren, ob die übertragenen Daten vollständig sind und dem erwarteten Format entsprechen.

</details>

<details>
<summary>🔗 Siehe auch</summary>

- [API](A.md#api)
- [Schnittstelle](S.md#schnittstelle)
- [[Webservice|Webservice]]
- [XML](X.md#xml)

</details>

## DOM

| Feld | Inhalt |
|------|--------|
| 🇬🇧 **Englisch** | Document Object Model |
| 🇩🇪 **Deutsch** | Dokumenten-Objektmodell |
| 🎯 **Wozu dient das?** | Das DOM bildet den Inhalt einer Webseite als geordnete Struktur ab. Dadurch können Browser und Programme einzelne Elemente finden, verändern oder ergänzen. |
| 🧠 **Merksatz** | **Das DOM ist der vom Browser aufgebaute Strukturbaum einer Webseite.** |

<details>
<summary>💡 Beispiel</summary>

Aus diesem HTML:

```html
<body>
  <h1>Willkommen</h1>
  <p>Das ist ein Text.</p>
</body>
```

erstellt der Browser vereinfacht diese Struktur:

```text
body
├── h1
│   └── Willkommen
└── p
    └── Das ist ein Text.
```

Die Überschrift und der Textabschnitt sind einzelne Elemente im DOM.

</details>

<details>
<summary>📚 Mehr wissen</summary>

Das DOM ist weder eine Programmiersprache noch eine Datei.

Es ist eine Darstellung, die der Browser aus dem HTML-Dokument erstellt. Über diese Struktur können Elemente beispielsweise:

- gefunden,
- ausgeblendet,
- verändert,
- verschoben,
- ergänzt oder
- gelöscht werden.

</details>

<details>
<summary>⚙️ Technischer Hintergrund</summary>

Die Elemente werden im DOM wie in einem Baum angeordnet. Elemente können dabei übergeordnete und untergeordnete Elemente besitzen.

JavaScript kann auf das DOM zugreifen und dadurch eine Webseite verändern, ohne dass die ganze Seite neu geladen werden muss.

CSS verwendet die HTML- beziehungsweise DOM-Struktur, um festzulegen, wie bestimmte Elemente dargestellt werden.

</details>

<details>
<summary>💼 Mein Arbeitsalltag</summary>

Bei dynamischen Benutzeroberflächen können Elemente abhängig von einer Auswahl erscheinen, verschwinden oder ihren Inhalt verändern.

Das DOM hilft mir zu verstehen, wie ein Browser die sichtbaren Elemente einer Webanwendung verwaltet.

</details>

<details>
<summary>🔗 Siehe auch</summary>

- [Browser](B.md#browser)
- [CSS](C.md#css)
- [HTML](H.md#html)
- [Rendern](R.md#rendern)

</details>