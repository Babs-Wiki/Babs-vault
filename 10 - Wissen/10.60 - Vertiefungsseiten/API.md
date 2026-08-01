# API

**API** steht für **Application Programming Interface**.

> **Merksatz:** Eine API definiert, wie zwei Programme miteinander kommunizieren dürfen.

---

<details>
<summary>📖 Definition</summary>

Eine API ist eine definierte Schnittstelle, über die verschiedene Programme miteinander kommunizieren können.

Sie legt fest:

- welche Anfragen erlaubt sind
- welche Daten übermittelt werden
- in welchem Format die Daten gesendet werden
- welche Antworten zurückgegeben werden
- welche Fehlermeldungen möglich sind

Man kann sich eine API wie ein Regelwerk oder einen standardisierten Fragebogen zwischen zwei Programmen vorstellen.

</details>

<details>
<summary>💡 Beispiel</summary>

Ein Polizeisystem benötigt Personendaten aus einem anderen System.

Das Polizeisystem sendet über die API eine Anfrage:

> Gib mir die Daten zur Person mit der Nummer 12345.

Die API definiert:

- wie die Anfrage aussehen muss
- welche Angaben erforderlich sind
- welche Daten zurückgegeben werden
- in welchem Format die Antwort erfolgt
- welche Fehlermeldungen möglich sind

Das anfragende Programm muss sich an diese Regeln halten.

</details>

<details>
<summary>🔗 API und Webservice</summary>

Die Begriffe **API** und **Webservice** werden häufig gemeinsam verwendet, bedeuten aber nicht genau dasselbe.

### API

Die API beschreibt die Regeln der Kommunikation.

Sie legt fest, welche Anfragen möglich sind und wie Daten ausgetauscht werden.

### Webservice

Der Webservice ist ein Dienst, der über ein Netzwerk erreichbar ist.

Er nimmt Anfragen entgegen, verarbeitet sie und sendet eine Antwort zurück.

> **Merksatz:**  
> API = Sprache und Regeln  
> Webservice = Dienst, der diese Sprache spricht

</details>

<details>
<summary>🎯 Warum sind APIs wichtig?</summary>

APIs ermöglichen:

- Datenaustausch zwischen verschiedenen Systemen
- Automatisierung von Prozessen
- Integration unterschiedlicher Anwendungen
- Wiederverwendung bestehender Funktionen
- klar geregelte Kommunikation
- kontrollierten Zugriff auf Daten und Funktionen

Ohne APIs müssten Programme direkt und individuell miteinander verbunden werden.

Das wäre komplizierter, fehleranfälliger und schwieriger zu warten.

</details>

<details>
<summary>⚙️ Technischer Hintergrund</summary>

Eine API kann verschiedene Arten von Anfragen anbieten.

Typische Aktionen sind:

- Daten abrufen
- neue Daten erstellen
- bestehende Daten ändern
- Daten löschen
- eine bestimmte Funktion auslösen

Anfrage und Antwort werden häufig in einem strukturierten Datenformat übertragen, beispielsweise:

- JSON
- XML

Viele Web-APIs verwenden HTTP oder HTTPS für die Kommunikation.

Für geschützte Daten werden normalerweise Berechtigungen oder andere Formen der Authentifizierung benötigt.

</details>

<details>
<summary>⚠️ Typische Fehler</summary>

Bei der Kommunikation über eine API können unter anderem folgende Probleme auftreten:

- falsches Datenformat
- fehlende Pflichtfelder
- ungültige Werte
- fehlende Berechtigungen
- Netzwerkprobleme
- Zeitüberschreitung
- Zielsystem nicht erreichbar
- Fehler im Webservice
- unerwartete Antwort des Zielsystems

Die API kann für solche Situationen definierte Fehlermeldungen oder Statuscodes zurückgeben.

</details>

<details>
<summary>💼 Mein Arbeitsalltag</summary>

APIs begegnen mir, wenn verschiedene Fachanwendungen Daten miteinander austauschen.

Bei Tests prüfe ich beispielsweise:

- ob eine Anfrage korrekt übermittelt wird
- ob alle benötigten Daten enthalten sind
- ob die Antwort vollständig ist
- ob Fehler richtig behandelt werden
- ob das empfangende System die Daten korrekt verarbeitet

</details>

<details>
<summary>🔗 Siehe auch</summary>

- [Webservice](Webservice.md)

</details>