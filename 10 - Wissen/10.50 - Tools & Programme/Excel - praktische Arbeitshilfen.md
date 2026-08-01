# Excel – praktische Arbeitshilfen

Diese Seite enthält praktische Excel-Funktionen, die das Arbeiten mit grossen Tabellen und Testlisten erleichtern.

> **Merksatz:** Eine gut aufgebaute Excel-Tabelle spart Zeit, verhindert Fehleingaben und erleichtert die Kontrolle von Daten.

---

## Index

- [Wertehilfe mit einer Auswahlliste](#wertehilfe)
- [Automatisch bis zur letzten Zeile ausfüllen](#automatisch)
- [Spalten ausblenden und einblenden](#spalten)
- [Filter verwenden](#filter)
- [Spalten mit Formeln sicher löschen](#formeln)
- [Datenprüfung übertragen](#datenregeln)
- [Nutzen beim Testing](#testing)
- [Mein Arbeitsalltag](#arbeitsalltag)

---

## Wertehilfe

**Wertehilfe mit einer Auswahlliste**

<details>
<summary>📋 Anleitung öffnen</summary>

Mit einer Wertehilfe können in einer Zelle nur vorgegebene Werte ausgewählt werden.

Das ist besonders hilfreich, wenn immer dieselben Einträge verwendet werden sollen.

Beispiele:

- Status
- Ja / Nein
- Test erfolgreich / nicht erfolgreich
- Priorität
- Zuständigkeit
- System oder Umgebung

### Vorbereitung

Die erlaubten Werte werden am besten in einem eigenen Tabellenblatt erfasst.

Beispiel:

```text
Offen
In Bearbeitung
Erledigt
Nicht relevant
```

Die Liste kann als Excel-Tabelle formatiert und eindeutig benannt werden.

### Auswahlliste erstellen

1. Die Zellen markieren, die eine Wertehilfe erhalten sollen.
2. Im Menü **Daten** auswählen.
3. **Datenüberprüfung** öffnen.
4. Unter **Zulassen** den Eintrag **Liste** wählen.
5. Als Quelle den Bereich mit den erlaubten Werten angeben.
6. Mit **OK** bestätigen.

Anschliessend erscheint in den Zellen eine Auswahlliste.

### Vorteile

- einheitliche Schreibweisen
- weniger Tippfehler
- schnellere Eingabe
- zuverlässigere Filter
- bessere Auswertung der Tabelle

> **Merksatz:** Eine Auswahlliste sorgt dafür, dass alle dieselben gültigen Werte verwenden.

</details>

[⬆️ Zurück zum Index](#index)

---

## Automatisch

**Automatisch bis zur letzten Zeile ausfüllen**

<details>
<summary>🔽 Anleitung öffnen</summary>

Excel kann einen Wert oder eine Formel automatisch nach unten übernehmen.

### Vorgehen

1. Die Zelle mit dem gewünschten Inhalt markieren.
2. Den Mauszeiger auf das kleine Quadrat unten rechts an der Zelle bewegen.
3. Auf dieses **Ausfüllkästchen** doppelklicken.

Excel übernimmt den Inhalt normalerweise bis zur letzten zusammenhängend gefüllten Zeile der benachbarten Spalte.

### Beispiel

In der ersten Zeile einer neuen Spalte steht eine Formel.

Durch einen Doppelklick auf das Ausfüllkästchen wird die Formel für alle vorhandenen Datensätze übernommen.

### Wichtig

Das automatische Ausfüllen funktioniert am zuverlässigsten, wenn die angrenzende Spalte keine unerwarteten Leerzeilen enthält.

> **Merksatz:** Doppelklick auf die rechte untere Zellenecke füllt die Spalte automatisch nach unten aus.

</details>

[⬆️ Zurück zum Index](#index)

---

## Spalten

**Spalten ausblenden und einblenden**

<details>
<summary>🙈 Anleitung öffnen</summary>

Spalten können ausgeblendet werden, wenn sie vorübergehend nicht benötigt werden, aber erhalten bleiben sollen.

### Spalte ausblenden

1. Die gewünschte Spalte markieren.
2. Mit der rechten Maustaste auf den Spaltenbuchstaben klicken.
3. **Ausblenden** auswählen.

### Spalte wieder einblenden

1. Die Spalten links und rechts der ausgeblendeten Spalte markieren.
2. Mit der rechten Maustaste auf einen der markierten Spaltenbuchstaben klicken.
3. **Einblenden** auswählen.

### Beispiel

Zwischen den Spalten `C` und `E` ist die Spalte `D` ausgeblendet.

Zum Einblenden werden die Spalten `C` und `E` gemeinsam markiert.

### Einsatz

Das Ausblenden ist hilfreich, wenn:

- technische Hilfsspalten nicht ständig sichtbar sein sollen
- eine grosse Tabelle übersichtlicher dargestellt werden soll
- nur bestimmte Spalten für eine Kontrolle relevant sind

> **Wichtig:** Ausgeblendete Spalten sind nicht gelöscht. Ihre Inhalte bleiben bestehen.

</details>

[⬆️ Zurück zum Index](#index)

---

## Filter

**Filter verwenden**

<details>
<summary>🔎 Anleitung öffnen</summary>

Filter helfen dabei, nur bestimmte Zeilen einer Tabelle anzuzeigen.

Damit können grosse Datenmengen schneller durchsucht und kontrolliert werden.

### Filter einschalten

1. Eine Zelle innerhalb der Tabelle auswählen.
2. Im Menü **Daten** auf **Filter** klicken.
3. In den Spaltenüberschriften erscheinen Filterpfeile.

### Mögliche Filter

Je nach Inhalt kann gefiltert werden nach:

- bestimmten Werten
- Text
- Zahlen
- Datum
- leeren oder nicht leeren Zellen
- mehreren ausgewählten Werten

### Beispiel

In einer Testtabelle kann nur der Status **Nicht erfolgreich** angezeigt werden.

Dadurch sind sofort alle Testfälle sichtbar, die nochmals geprüft werden müssen.

### Sortieren und Filtern

- **Sortieren** verändert die Reihenfolge der sichtbaren Datensätze.
- **Filtern** blendet nicht passende Datensätze vorübergehend aus.

> **Merksatz:** Sortieren ordnet die Daten – Filtern zeigt nur die benötigten Daten.

</details>

[⬆️ Zurück zum Index](#index)

---

## Formeln

**Spalten mit Formeln sicher löschen**

<details>
<summary>🧮 Anleitung öffnen</summary>

Beim Löschen von Zellen oder ganzen Spalten ist Vorsicht nötig, wenn Formeln beteiligt sind.

Eine Formel kann:

- direkt in der zu löschenden Spalte stehen
- auf Werte aus dieser Spalte zugreifen
- von anderen Formeln weiterverwendet werden

Wird eine benötigte Spalte gelöscht, kann beispielsweise der Fehler `#BEZUG!` entstehen.

### Vor dem Löschen prüfen

- Enthält die Spalte Formeln?
- Greifen andere Formeln auf diese Spalte zu?
- Werden die Werte für Berechnungen, Filter oder Auswertungen benötigt?
- Sind ausgeblendete Hilfsspalten betroffen?
- Muss vor der Änderung eine Sicherungskopie erstellt werden?

### Formelabhängigkeiten anzeigen

Unter **Formeln → Formelüberwachung** können unter anderem folgende Funktionen verwendet werden:

- **Spur zum Vorgänger**  
  Zeigt, aus welchen Zellen eine Formel ihre Werte bezieht.

- **Spur zum Nachfolger**  
  Zeigt, welche anderen Formeln die ausgewählte Zelle verwenden.

### Sicheres Vorgehen

1. Betroffene Spalte kontrollieren.
2. Vorhandene Formeln und Abhängigkeiten prüfen.
3. Bei Unsicherheit eine Kopie der Datei speichern.
4. Spalte löschen.
5. Berechnungen und Fehlermeldungen kontrollieren.
6. Wichtige Filter und Auswertungen erneut testen.

> **Merksatz:** Vor dem Löschen einer Spalte prüfen, ob andere Formeln von ihr abhängig sind.

</details>

[⬆️ Zurück zum Index](#index)

---

## Datenregeln

**Datenprüfung auf neue Zellen oder Spalten übertragen**

<details>
<summary>📋 Anleitung öffnen</summary>

Eine bereits eingerichtete Datenprüfung kann als Vorlage für weitere Zellen oder Spalten verwendet werden.

Dadurch erhalten die neuen Felder dieselben:

- Auswahlwerte
- Eingaberegeln
- Fehlermeldungen
- Dropdown-Listen

### Nur die Datenprüfung kopieren

1. Eine Zelle mit funktionierender Datenprüfung markieren.
2. Die Zelle mit `Ctrl + C` kopieren.
3. Die neuen Zielzellen markieren.
4. **Inhalte einfügen** öffnen.
5. **Datenüberprüfung** beziehungsweise **Gültigkeit** auswählen.

Dadurch wird nur die Datenprüfung übernommen. Der vorhandene Zellinhalt und andere Formatierungen bleiben grundsätzlich bestehen.

### Anschliessend kontrollieren

- Erscheint die gewünschte Dropdown-Liste?
- Werden alle erlaubten Werte angezeigt?
- Verweist die Datenprüfung auf den richtigen Bereich?
- Werden ungültige Eingaben verhindert oder gemeldet?
- Funktioniert die Wertehilfe auch in neu hinzugefügten Zeilen?

### Vorteil einer bestehenden Vorlage

Eine bereits korrekt konfigurierte Zelle spart Zeit und verhindert, dass Regeln für neue Spalten unterschiedlich eingerichtet werden.

> **Merksatz:** Eine funktionierende Zelle kann als Vorlage für dieselbe Datenprüfung verwendet werden.

</details>

[⬆️ Zurück zum Index](#index)

---

## Testing

**Nutzen beim Testing**

<details>
<summary>🧪 Inhalt öffnen</summary>

Gut aufgebaute Excel-Tabellen können beim Testing helfen:

- Testfälle übersichtlich zu ordnen
- erlaubte Werte über Auswahllisten vorzugeben
- Ergebnisse einheitlich zu dokumentieren
- fehlgeschlagene Tests schnell zu filtern
- Formeln oder Werte automatisch zu übernehmen
- nicht benötigte Hilfsspalten auszublenden
- offene Punkte schneller zu erkennen

Mögliche Spalten einer allgemeinen Testliste:

| Spalte | Inhalt |
|---|---|
| Testfall | Was wird geprüft? |
| Erwartetes Ergebnis | Was sollte geschehen? |
| Tatsächliches Ergebnis | Was ist tatsächlich geschehen? |
| Status | Erfolgreich / nicht erfolgreich |
| Bemerkung | Zusätzliche Beobachtungen |
| Datum | Zeitpunkt des Tests |

Im privaten Wiki werden nur allgemeine Vorgehensweisen dokumentiert.

Firmeninterne Testdaten, Systemangaben und vertrauliche Informationen gehören nicht hinein.

</details>

[⬆️ Zurück zum Index](#index)

---

## Arbeitsalltag

**Mein Arbeitsalltag**

<details>
<summary>💼 Inhalt öffnen</summary>

Diese Excel-Funktionen helfen mir insbesondere bei grossen Tabellen:

- Werte über Auswahllisten einheitlich erfassen
- Inhalte oder Formeln schnell nach unten übernehmen
- nicht benötigte Spalten vorübergehend ausblenden
- bestimmte Teststände oder Ergebnisse filtern
- Fehler und offene Punkte schneller finden

> **Erkenntnis:** Gut vorbereitete Tabellen reduzieren wiederholte Handarbeit und erleichtern die Kontrolle.

</details>

[⬆️ Zurück zum Index](#index)