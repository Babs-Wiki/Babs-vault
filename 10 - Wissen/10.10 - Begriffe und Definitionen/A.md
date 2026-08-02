
## Begriffe


- [Alerting](#alerting)
- [API](#api)
- [Assignee](#assignee)
- [Asynchron](S.md#synchron-und-asynchron)
- [Authentifizierung](#authentifizierung)

---

# API

| Bereich | Inhalt |
|---|---|
| 🇬🇧 Englisch | Application Programming Interface |
| 🇩🇪 Deutsch | Programmierschnittstelle |
| 🎯 Wozu dient das? | Eine API ermöglicht es Programmen, miteinander zu kommunizieren und Daten auszutauschen. |
| 🧠 Merksatz | **API = Übersetzer zwischen zwei Programmen.** |

<details>
<summary>💡 Beispiel</summary>

Eine Wetter-App zeigt die Wetterdaten an.

Sie misst das Wetter nicht selbst, sondern fragt über eine API einen Wetterdienst an und erhält die aktuellen Daten zurück.

</details>

<details>
<summary>📚 Mehr wissen</summary>

APIs werden heute fast überall eingesetzt.

Zum Beispiel:

- Wetter-Apps
- Online-Shops
- Zahlungsdienste
- Microsoft 365
- SAP
- ChatGPT

</details>

<details>
<summary>⚙️ Technischer Hintergrund</summary>

Eine API legt fest, welche Daten angefragt werden dürfen und in welchem Format die Antwort zurückkommt.

Häufig werden Daten als JSON oder XML übertragen.

</details>

<details>
<summary>💼 Mein Arbeitsalltag</summary>

Bei der Kantonspolizei Bern begegnen dir APIs häufig indirekt.

Wenn zwei Anwendungen Informationen austauschen oder ein Webservice Daten liefert, steckt meistens eine API dahinter.

</details>

<details>
<summary>🔗 Siehe auch</summary>

- [Webservice](../10.60%20-%20Vertiefungsseiten/Webservice.md)]
- [XML](X.md#xml)
- [JSON](J.md#json)
- [Frontend](F.md#frontend)
- [Backend](B.md#backend)

</details>

---

### Synchron und asynchron

| Begriff | Deutsch | Merksatz |
|----------|---------|----------|
| **Synchron / asynchron** | Wartend / unabhängig weiterarbeitend | **Synchron wartet auf die Antwort – asynchron arbeitet währenddessen weiter.** |

Bei einer **synchronen** Verarbeitung wartet der Aufrufer, bis eine Aufgabe abgeschlossen ist und eine Antwort zurückkommt.

Bei einer **asynchronen** Verarbeitung kann der Aufrufer weiterarbeiten. Die Antwort oder das Ergebnis wird später geliefert.

<details>
<summary>💡 Beispiel</summary>

**Synchron:**

Eine Anwendung fragt Daten bei einem Server ab. Bis die Antwort kommt, kann sie an dieser Stelle nicht weiterarbeiten.

**Asynchron:**

Eine Anwendung startet einen längeren Datenexport. Während der Export läuft, kann die Benutzerin weitere Aufgaben erledigen. Nach Abschluss erscheint eine Benachrichtigung.

</details>

<details>
<summary>📚 Mehr Wissen</summary>

Synchrone Abläufe sind oft einfacher zu verstehen und umzusetzen.

Asynchrone Abläufe eignen sich besonders für Aufgaben, die länger dauern oder unabhängig im Hintergrund ausgeführt werden können.

Typische Beispiele sind:

- Datei-Uploads
- Datenexporte
- E-Mail-Versand
- Hintergrundverarbeitung
- Nachrichtenwarteschlangen

</details>

<details>
<summary>⚙️ Technik</summary>

Synchron wird häufig auch als **blockierend** bezeichnet, weil der weitere Ablauf bis zur Antwort blockiert ist.

Asynchron wird häufig mit folgenden Techniken umgesetzt:

- Callbacks
- Promises
- Events
- Warteschlangen
- Hintergrundprozesse

Asynchron bedeutet nicht automatisch, dass mehrere Aufgaben gleichzeitig ausgeführt werden. Es bedeutet zunächst nur, dass nicht auf den Abschluss gewartet werden muss.

</details> 

### Assignee

| Begriff | Deutsch | Merksatz |
|----------|----------|----------|
| **Assignee** | Zuständige Person / Bearbeiter | **Der Assignee ist die Person, die für die Aufgabe verantwortlich ist.** |

Die Person, der ein Ticket, eine Aufgabe oder ein Vorgang zur Bearbeitung zugewiesen wurde.

<details>
<summary>💡 Beispiel</summary>

Im Jira-Ticket steht:

**Assignee:** Barbara Muster

Barbara ist für die Bearbeitung dieses Tickets verantwortlich.

</details>

<details>
<summary>📚 Mehr Wissen</summary>

Der Assignee kann während der Bearbeitung geändert werden. Fast jedes Ticketsystem (z. B. Jira oder Azure DevOps) verwendet einen Assignee.

</details>

<details>
<summary>⚙️ Technik</summary>

Der Assignee ist ein Benutzerkonto im Ticketsystem und dient der Zuweisung sowie Nachverfolgung von Aufgaben.

</details>

### Alerting

| Begriff | Deutsch | Merksatz |
|----------|---------|----------|
| **Alerting** | Automatische Alarmierung oder Benachrichtigung | **Alerting meldet automatisch, wenn etwas Aufmerksamkeit benötigt.** |

Alerting bezeichnet die automatische Benachrichtigung bei Fehlern, Warnungen oder wichtigen Ereignissen in einem System.

<details>
<summary>💡 Beispiel</summary>

Ein Server ist nicht mehr erreichbar.

Das Überwachungssystem sendet automatisch eine Meldung an das zuständige Informatikteam.

</details>

<details>
<summary>📚 Mehr Wissen</summary>

Ein Alert kann beispielsweise ausgelöst werden, wenn:

- ein System ausfällt
- ein Fehler häufig auftritt
- der Speicherplatz knapp wird
- eine Antwortzeit zu hoch ist
- ein Sicherheitsereignis erkannt wird

Benachrichtigungen können per E-Mail, SMS, Chat oder über ein Ticketsystem versendet werden.

</details>

<details>
<summary>⚙️ Technik</summary>

Alerting baut meistens auf einem Monitoring-System auf.

**Monitoring** sammelt und überwacht Messwerte.

**Alerting** reagiert darauf, wenn ein definierter Grenzwert überschritten oder eine bestimmte Bedingung erfüllt wird.

Zu viele unwichtige Meldungen können zu **Alert Fatigue** führen. Dabei werden wichtige Warnungen möglicherweise übersehen.

</details>

### Authentifizierung

| Feld | Inhalt |
|------|--------|
| 🇬🇧 **Englisch** | Authentication |
| 🇩🇪 **Deutsch** | Authentifizierung / Identitätsprüfung |
| 🎯 **Wozu dient das?** | Bei der Authentifizierung prüft ein System, ob eine Person oder ein anderes System wirklich die angegebene Identität besitzt. |
| 🧠 **Merksatz** | **Authentifizierung beantwortet die Frage: Wer bist du?** |

<details>
<summary>💡 Beispiel</summary>

Bei der Anmeldung kann die Identität beispielsweise geprüft werden durch:

- Benutzername und Passwort,
- Fingerabdruck oder Gesichtserkennung,
- einen Bestätigungscode,
- eine Anmeldung über Apple oder einen anderen Anbieter.

Bei meiner ChatGPT-Anmeldung bestätigt Apple gegenüber ChatGPT, dass ich erfolgreich bei Apple angemeldet wurde.

</details>

<details>
<summary>📚 Mehr wissen</summary>

Authentifizierung und Berechtigung sind nicht dasselbe:

- **Authentifizierung:** Wer bist du?
- **Autorisierung:** Was darfst du?

Nach einer erfolgreichen Authentifizierung erhält eine Person häufig ein Token. Dieses dient danach als digitaler Nachweis für die laufende Sitzung.

</details>

<details>
<summary>⚙️ Technischer Hintergrund</summary>

Nach der erfolgreichen Identitätsprüfung kann ein System ein zeitlich begrenztes Token ausstellen.

Bei späteren Anfragen wird dieses Token mitgesendet. Dadurch muss das Passwort nicht bei jeder einzelnen Aktion erneut übertragen werden.

</details>

<details>
<summary>💼 Mein Arbeitsalltag</summary>

Authentifizierung begegnet mir bei der Anmeldung an Anwendungen, bei Benutzerkonten und bei Schnittstellen.

Bei Tests kann ich beispielsweise prüfen, ob eine Anmeldung funktioniert und ob nicht angemeldete Personen korrekt abgewiesen werden.

</details>

<details>
<summary>🔗 Siehe auch</summary>

- [OAuth](O.md#oauth)
- [Token](T.md#token)

</details>