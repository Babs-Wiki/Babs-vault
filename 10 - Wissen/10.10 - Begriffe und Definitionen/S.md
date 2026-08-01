- [Scope](#scope)
- [Smart Value Help](#smart-value-help)
- [Synchron und asynchron](#synchron-und-asynchron)

### Scope

| Begriff | Deutsch | Merksatz |
|----------|---------|----------|
| **Scope** | Umfang / Geltungsbereich | **Der Scope legt fest, was zu einer Aufgabe oder einem Projekt gehört – und was nicht.** |

Der Scope beschreibt den festgelegten Umfang eines Projekts, einer Aufgabe oder einer Änderung.

<details>
<summary>💡 Beispiel</summary>

Bei einer Softwareänderung gehört das Anpassen einer Eingabemaske zum Scope.

Eine zusätzliche neue Suchfunktion gehört nicht zum Scope und müsste separat beauftragt werden.

</details>

<details>
<summary>📚 Mehr Wissen</summary>

Ein klar definierter Scope verhindert Missverständnisse und ungeplante Zusatzarbeiten.

Wird ein Projekt während der Umsetzung immer weiter erweitert, spricht man von **Scope Creep**.

</details>

<details>
<summary>⚙️ Technik</summary>

Der Scope kann beispielsweise festlegen:

- welche Funktionen verändert werden
- welche Systeme betroffen sind
- welche Testfälle durchgeführt werden
- welche Anforderungen ausdrücklich nicht dazugehören

</details>

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

### Smart Value Help

| Begriff | Deutsch | Merksatz |
|----------|---------|----------|
| **Smart Value Help** | Intelligente Such- und Auswahlhilfe | **Smart Value Help unterstützt bei der Auswahl eines gültigen Wertes.** |

Smart Value Help ist eine intelligente Eingabehilfe, die während der Eingabe passende und erlaubte Werte sucht und zur Auswahl anbietet.

<details>
<summary>💡 Beispiel</summary>

In einem Feld muss eine Organisationseinheit eingetragen werden.

Nach der Eingabe der ersten Buchstaben zeigt das System passende Organisationseinheiten an. Die Benutzerin kann den richtigen Wert auswählen, statt ihn vollständig einzugeben.

</details>

<details>
<summary>📚 Mehr Wissen</summary>

Eine Value Help kann beispielsweise Folgendes anbieten:

- Suchvorschläge
- Trefferlisten
- Filtermöglichkeiten
- zusätzliche Beschreibungen
- Auswahl gültiger Werte

Dadurch werden Tippfehler und ungültige Eingaben verhindert.

</details>

<details>
<summary>⚙️ Technik</summary>

Die vorgeschlagenen Werte können aus einer Datenbank oder über einen Webservice geladen werden.

Die Value Help kann abhängig von bereits ausgefüllten Feldern gefiltert werden.

Beispielsweise werden nach der Auswahl eines Landes nur noch Orte aus diesem Land vorgeschlagen.

Der genaue Funktionsumfang hängt von der verwendeten Anwendung oder dem eingesetzten Framework ab.

</details>