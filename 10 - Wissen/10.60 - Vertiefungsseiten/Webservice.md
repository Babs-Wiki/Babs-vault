

Ein **Webservice** ermöglicht den Datenaustausch zwischen verschiedenen Programmen oder Systemen über ein Netzwerk.

> **Merksatz:** Ein Webservice nimmt Anfragen eines Systems entgegen, verarbeitet sie und liefert eine Antwort zurück.

---

<details>
<summary>📖 Definition</summary>

Ein Webservice ist ein Dienst, über den verschiedene Programme oder Systeme miteinander kommunizieren können.

Ein System sendet eine Anfrage. Der Webservice verarbeitet diese Anfrage und liefert anschliessend eine Antwort zurück.

Dabei können beispielsweise:

- Daten abgefragt werden
- neue Daten übermittelt werden
- bestehende Daten geändert werden
- Prüfungen durchgeführt werden
- bestimmte Aktionen ausgelöst werden

Ein Webservice besitzt meistens eine definierte API. Diese legt fest, wie die Anfragen und Antworten aufgebaut sein müssen.

</details>

<details>
<summary>🔄 Ablauf einer Webservice-Anfrage</summary>

Eine Webservice-Kommunikation läuft vereinfacht in folgenden Schritten ab:

1. Ein System erstellt eine Anfrage.
2. Die Anfrage wird an den Webservice gesendet.
3. Der Webservice prüft die übermittelten Daten.
4. Die Anfrage wird verarbeitet oder an ein Zielsystem weitergeleitet.
5. Das Ergebnis wird als Antwort zurückgesendet.
6. Das anfragende System verarbeitet die Antwort.

Vereinfacht dargestellt:

```text
Anwendung
   ↓ Anfrage
Webservice
   ↓ Verarbeitung oder Weiterleitung
Zielsystem
   ↑ Ergebnis
Webservice
   ↑ Antwort
Anwendung
```

</details>

<details>
<summary>💡 Beispiel</summary>

SAP benötigt Daten aus einem anderen System.

SAP sendet über einen Webservice eine Anfrage:

> Gib mir die Daten zur Person mit der Nummer 12345.

Der Webservice:

1. nimmt die Anfrage entgegen
2. prüft die übermittelten Angaben
3. fragt die Daten im Zielsystem ab
4. liefert die gefundenen Daten an SAP zurück

Falls die Person nicht gefunden wird oder ein Fehler auftritt, sendet der Webservice eine entsprechende Fehlermeldung zurück.

</details>

<details>
<summary>🔗 API und Webservice</summary>

Die Begriffe **API** und **Webservice** werden häufig gemeinsam verwendet, bedeuten aber nicht genau dasselbe.

### API

Die API beschreibt die Regeln der Kommunikation.

Sie legt beispielsweise fest:

- welche Anfragen erlaubt sind
- welche Angaben erforderlich sind
- wie die Daten aufgebaut sein müssen
- welche Antworten möglich sind
- welche Fehlermeldungen zurückgegeben werden

### Webservice

Der Webservice ist der über ein Netzwerk erreichbare Dienst, der die Anfrage entgegennimmt und verarbeitet.

> **Merksatz:**  
> API = Sprache und Regeln  
> Webservice = Dienst, der diese Sprache versteht

</details>

<details>
<summary>☑️ Checkboxen im Webservice-Kontext</summary>

Checkboxen können Optionen oder das Verhalten einer Webservice-Anfrage steuern.

Beispiele:

- ☑️ Daten speichern
- ☐ Nur prüfen
- ☑️ Synchronisation starten

Je nachdem, ob eine Checkbox gesetzt ist, wird eine bestimmte Funktion aktiviert oder deaktiviert.

Technisch wird der Zustand häufig als Wahrheitswert übermittelt:

- `true` = Checkbox ist gesetzt
- `false` = Checkbox ist nicht gesetzt

Beispiel in XML:

```xml
<Anfrage>
  <DatenSpeichern>true</DatenSpeichern>
  <NurPruefen>false</NurPruefen>
  <SynchronisationStarten>true</SynchronisationStarten>
</Anfrage>
```

Der Webservice wertet diese Werte aus und führt die entsprechenden Aktionen aus.

Eine falsch gesetzte Checkbox kann deshalb dazu führen, dass:

- Daten nur geprüft, aber nicht gespeichert werden
- eine unerwünschte Aktion ausgelöst wird
- eine benötigte Verarbeitung nicht stattfindet
- der Webservice eine Fehlermeldung zurückgibt

</details>

<details>
<summary>⚠️ Typische Webservice-Fehler</summary>

Ein Fehler bei einer Webservice-Anfrage muss nicht zwingend durch den Webservice selbst verursacht werden.

Die Ursache kann auch in den Daten, den Berechtigungen, der Verbindung oder im Zielsystem liegen.

### XML- oder Datenfehler

- falsche Struktur
- fehlende Tags oder Felder
- ungültige Werte
- falsches Datenformat
- unzulässige Sonderzeichen
- falscher Datentyp

### Netzwerkprobleme

- Zielsystem nicht erreichbar
- Verbindung unterbrochen
- Netzwerk nicht verfügbar
- Zeitüberschreitung beziehungsweise Timeout
- falsche Netzwerkadresse

### Berechtigungsfehler

- Benutzer besitzt keinen Zugriff
- Anmeldung fehlgeschlagen
- Token ist ungültig oder abgelaufen
- benötigte Rolle fehlt
- Zugriff wurde verweigert

### Falsche Parameter

- Pflichtfelder fehlen
- ungültige ID
- falscher Wert wurde übermittelt
- Checkbox ist falsch gesetzt
- Suchkriterien sind unvollständig

### Fehler im Webservice

- Fehler in der Verarbeitung
- Programmfehler
- falsche Konfiguration
- unerwartete Antwort
- Dienst ist nicht verfügbar

### Fehler im Zielsystem

Der Webservice ist erreichbar und verarbeitet die Anfrage korrekt, aber das Zielsystem kann die Anfrage nicht abschliessen.

Mögliche Ursachen:

- Datenbankfehler
- Zielsystem ist überlastet
- benötigte Daten fehlen
- Geschäftsregel verhindert die Verarbeitung
- Fehler in einer nachgelagerten Anwendung

> **Merksatz:** Ein Webservice-Fehler liegt nicht immer am Webservice selbst. Häufig liegt die Ursache in den Daten, den Berechtigungen, der Verbindung oder im Zielsystem.

</details>

<details>
<summary>⚙️ Technischer Hintergrund</summary>

Webservices verwenden häufig HTTP oder HTTPS für die Kommunikation.

Anfragen und Antworten werden meist in einem strukturierten Datenformat übertragen, beispielsweise:

- XML
- JSON

Eine Webservice-Anfrage kann synchron oder asynchron verarbeitet werden.

### Synchron

Das anfragende System wartet, bis der Webservice eine Antwort zurücksendet.

### Asynchron

Das anfragende System arbeitet weiter. Das Ergebnis wird später bereitgestellt oder über eine weitere Nachricht übermittelt.

Für geschützte Webservices werden häufig folgende Sicherheitsmechanismen eingesetzt:

- Benutzername und Passwort
- Token
- Zertifikate
- Rollen und Berechtigungen
- verschlüsselte HTTPS-Verbindungen

</details>

<details>
<summary>💼 Mein Arbeitsalltag</summary>

Webservices begegnen mir, wenn verschiedene Fachanwendungen Daten miteinander austauschen.

Bei Tests kann ich beispielsweise prüfen:

- Wird die Anfrage korrekt übermittelt?
- Sind alle Pflichtfelder vorhanden?
- Sind Checkboxen und Parameter richtig gesetzt?
- Ist das XML korrekt aufgebaut?
- Wird die erwartete Antwort zurückgegeben?
- Werden Fehler verständlich gemeldet?
- Wird die Antwort im empfangenden System richtig verarbeitet?
- Liegt ein Fehler beim Webservice oder bei einem anderen beteiligten System?

Dabei ist wichtig, nicht nur die sichtbare Fehlermeldung zu betrachten, sondern den gesamten Weg der Anfrage zu prüfen.

</details>

<details>
<summary>🔗 Siehe auch</summary>

- [API](API.md)


</details>