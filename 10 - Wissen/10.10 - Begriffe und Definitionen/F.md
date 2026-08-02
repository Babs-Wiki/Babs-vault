

- [Frontend](#frontend)
- [Full Load](D.md#delta-load-und-full-load)

### Frontend

| Bereich | Inhalt |
|---|---|
| 🇬🇧 Englisch | Frontend |
| 🇩🇪 Deutsch | Benutzeroberfläche / sichtbarer Teil einer Anwendung |
| 🎯 Wozu dient das? | Das Frontend zeigt Informationen an und ermöglicht den Benutzerinnen und Benutzern, eine Anwendung zu bedienen und Eingaben zu machen. |
| 🧠 Merksatz | **Das Frontend ist der Teil einer Anwendung, den die Benutzerin sieht und bedient.** |

<details>
<summary>💡 Beispiel</summary>

Bei einer Fachanwendung gehören zum Frontend beispielsweise:

- Eingabefelder
- Checkboxen
- Dropdown-Listen
- Suchmasken
- Schaltflächen
- Tabellen
- Fehlermeldungen
- angezeigte Suchergebnisse

Eine Benutzerin gibt im Frontend eine Personen-ID ein und klickt auf **Suchen**.

Das Frontend sendet die Anfrage an das Backend und zeigt anschliessend die erhaltenen Daten an.

</details>

<details>
<summary>📚 Mehr wissen</summary>

Das Frontend ist für die Darstellung und Bedienung einer Anwendung verantwortlich.

Es soll unter anderem:

- verständlich aufgebaut sein
- Eingaben entgegennehmen
- gültige Werte unterstützen
- Fehlermeldungen anzeigen
- Ergebnisse übersichtlich darstellen
- auf verschiedene Bildschirmgrössen reagieren

Das Frontend enthält normalerweise nicht die gesamte fachliche Verarbeitung oder dauerhafte Datenspeicherung.

</details>

<details>
<summary>⚙️ Technischer Hintergrund</summary>

Bei Webanwendungen wird das Frontend häufig mit folgenden Technologien erstellt:

- HTML für die Struktur
- CSS für die Gestaltung
- JavaScript für Verhalten und Interaktion

Zusätzlich können Frameworks wie React, Angular oder Vue verwendet werden.

Das Frontend kommuniziert häufig über eine API mit dem Backend.

Vereinfacht:

```text
Benutzerin
    ↓
Frontend
    ↓ Anfrage
API / Webservice
    ↓
Backend
    ↑ Antwort
Frontend
    ↑
Benutzerin sieht das Ergebnis
```

</details>

<details>
<summary>💼 Mein Arbeitsalltag</summary>

Beim Testen des Frontends kann ich beispielsweise prüfen:

- Sind alle Felder sichtbar?
- Funktionieren Checkboxen und Dropdown-Listen?
- Werden gültige Werte angeboten?
- Sind Pflichtfelder gekennzeichnet?
- Werden Fehlermeldungen verständlich angezeigt?
- Entsprechen die angezeigten Daten der Antwort des Backends?
- Wird eine Eingabe korrekt gespeichert oder weitergeleitet?

Ein sichtbarer Fehler im Frontend muss nicht zwingend dort entstanden sein.

Die Ursache kann auch im Backend, im Webservice oder in den gelieferten Daten liegen.

</details>

<details>
<summary>🔗 Siehe auch</summary>

- [Backend](B.md#backend)
- [API](A.md#api)
- [[Webservice|Webservice]]
- [JSON](J.md#json)
- [XML](X.md#xml)

</details>