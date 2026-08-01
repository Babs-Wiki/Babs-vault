
- [Delta Load und Full Load](#delta-load-und-full-load)

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