# API

|  |  |
|---|---|
| 🇬🇧 **Englisch** | Application Programming Interface |
| 🇩🇪 **Deutsch** | Programmierschnittstelle |
| 🎯 **Wozu dient das?** | Damit Programme miteinander kommunizieren und Daten austauschen können. |
| 🧠 **Merksatz** | **API = Übersetzer zwischen Programmen.** |

---

<details>
<summary>💡 <strong>Beispiel</strong></summary>

Eine Polizei-App benötigt Angaben zu einer Person, die in einem anderen System gespeichert sind.

```text
Polizei-App
     │
     │ Anfrage
     ▼
    API
     │
     │ Datenabfrage
     ▼
Datenführendes System
     │
     │ Antwort
     ▼
Polizei-App
```

Die App greift nicht direkt auf die Datenbank des anderen Systems zu.  
Sie stellt ihre Anfrage über die API und erhält eine festgelegte Antwort zurück.

Ein einfaches Alltagsbeispiel:

> Die App fragt: „Gib mir die Daten zu dieser ID.“  
> Die API prüft die Anfrage und liefert die erlaubten Daten zurück.

</details>

<details>
<summary>📚 <strong>Mehr wissen</strong></summary>

Eine API legt fest, **wie zwei Programme miteinander kommunizieren dürfen**.

Sie beschreibt beispielsweise:

- welche Anfragen möglich sind,
- welche Angaben mitgegeben werden müssen,
- welche Daten zurückgegeben werden,
- in welchem Format die Antwort erfolgt,
- und welche Berechtigungen erforderlich sind.

Die beteiligten Programme müssen ihren inneren Aufbau nicht gegenseitig kennen.  
Sie müssen lediglich die vereinbarten Regeln der API einhalten.

Das kann man mit einem Restaurant vergleichen:

- Der Gast ist die anfragende Anwendung.
- Die Küche ist das datenverarbeitende System.
- Die Speisekarte beschreibt die verfügbaren Möglichkeiten.
- Die Bedienung übermittelt Bestellung und Ergebnis.

Die API übernimmt dabei sinngemäss die Rolle der Bedienung und der festgelegten Bestellregeln.

</details>

<details>
<summary>⚙️ <strong>Technischer Hintergrund</strong></summary>

Viele moderne APIs übertragen Daten über ein Netzwerk und verwenden dabei häufig:

- **HTTP oder HTTPS** für die Übertragung,
- **JSON oder XML** als Datenformat,
- **Token** zur Authentifizierung,
- **REST** oder **SOAP** als technische Architektur beziehungsweise Kommunikationsform.

Typische Aktionen einer API können sein:

```text
GET     → Daten lesen
POST    → neue Daten erstellen
PUT     → vorhandene Daten vollständig ändern
PATCH   → einzelne Daten ändern
DELETE  → Daten löschen
```

Eine API kann ausserdem festlegen:

- welche Felder übermittelt werden,
- welche Filter erlaubt sind,
- wie Fehler gemeldet werden,
- wie viele Anfragen zulässig sind,
- und welche Benutzer oder Systeme Zugriff erhalten.

Eine API ist nicht zwingend über das Internet erreichbar. Sie kann auch nur innerhalb eines geschützten Unternehmensnetzwerks verwendet werden.

</details>

<details>
<summary>💼 <strong>Mein Arbeitsalltag</strong></summary>

Der Begriff API kann dir unter anderem begegnen bei:

- Webservices,
- Dataverse und Power Apps,
- OData-Abfragen,
- XML- oder JSON-Daten,
- Tests zwischen unterschiedlichen Anwendungen,
- Fehlermeldungen beim Datenaustausch.

Bei einem Fehler kann beispielsweise geprüft werden:

- Wurde die Anfrage korrekt gesendet?
- Waren alle Pflichtfelder vorhanden?
- War die Berechtigung gültig?
- Hat das Zielsystem geantwortet?
- War die Antwort im erwarteten Format?

</details>

<details>
<summary>🔗 <strong>Siehe auch</strong></summary>

- [[Webservice]]
- [[XML]]
- [[JSON]]
- [[OData]]
- [[Token]]
- [[REST]]
- [[SOAP]]

</details>

---