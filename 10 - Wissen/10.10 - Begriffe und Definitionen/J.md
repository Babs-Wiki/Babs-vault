
- [JSON](#json)

### JSON

| Bereich | Inhalt |
|---|---|
| 🇬🇧 Englisch | JavaScript Object Notation |
| 🇩🇪 Deutsch | JavaScript-Objektnotation / strukturiertes Datenformat |
| 🎯 Wozu dient das? | JSON dient dazu, strukturierte Daten übersichtlich zu speichern und zwischen verschiedenen Programmen oder Systemen auszutauschen. |
| 🧠 Merksatz | **JSON verpackt Daten als übersichtliche Schlüssel-Wert-Paare.** |

<details>
<summary>💡 Beispiel</summary>

Personendaten können in JSON so dargestellt werden:

```json
{
  "personenID": 12345,
  "vorname": "Anna",
  "nachname": "Muster",
  "ort": "Thun",
  "aktiv": true
}
```

Dabei ist beispielsweise:

- `"vorname"` der Schlüssel
- `"Anna"` der zugehörige Wert
- `"aktiv": true` ein Wahrheitswert

</details>

<details>
<summary>📚 Mehr wissen</summary>

JSON wird häufig verwendet für:

- Webservices
- APIs
- Konfigurationsdateien
- Datenaustausch zwischen Frontend und Backend
- Antworten von Servern
- Speicherung strukturierter Einstellungen

JSON ist meist kompakter als XML und deshalb bei modernen Webanwendungen weit verbreitet.

</details>

<details>
<summary>⚙️ Technischer Hintergrund</summary>

JSON unterstützt verschiedene Datentypen:

| Datentyp | Beispiel |
|---|---|
| Text | `"name": "Anna"` |
| Zahl | `"alter": 35` |
| Wahrheitswert | `"aktiv": true` |
| Leerer Wert | `"bemerkung": null` |
| Liste | `"rollen": ["Admin", "Support"]` |
| Objekt | `"adresse": {"ort": "Thun"}` |

Wichtige Regeln:

- Objekte stehen zwischen `{ }`.
- Listen stehen zwischen `[ ]`.
- Schlüssel stehen in doppelten Anführungszeichen.
- Schlüssel und Wert werden durch einen Doppelpunkt getrennt.
- Mehrere Einträge werden durch Kommas getrennt.

Ein fehlendes Komma oder Anführungszeichen kann dazu führen, dass das JSON nicht verarbeitet werden kann.

</details>

<details>
<summary>💼 Mein Arbeitsalltag</summary>

JSON kann mir begegnen, wenn ich:

- eine Anfrage oder Antwort eines Webservices prüfe
- übermittelte Felder kontrolliere
- Pflichtfelder suche
- Werte und Datentypen vergleiche
- eine Fehlermeldung wegen einer ungültigen Datenstruktur untersuche

Dabei kann ich prüfen:

- Sind alle erwarteten Felder vorhanden?
- Stimmen Feldnamen und Werte?
- Besitzen Zahlen, Texte und Wahrheitswerte den richtigen Datentyp?
- Ist die Struktur vollständig und korrekt?

</details>

<details>
<summary>🔗 Siehe auch</summary>

- [API](A.md#api)
- [Webservice](W.md#webservice)
- [XML](X.md#xml)
- [Frontend](F.md#frontend)
- [Backend](B.md#backend)

</details>