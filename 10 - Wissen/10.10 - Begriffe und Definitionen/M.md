## Begriffe

- [Mapping](#mapping)
- [markdown](#markdown)

# Markdown

| Bereich | Inhalt |
|---|---|
| 🇬🇧 Englisch | Markdown |
| 🇩🇪 Deutsch | Einfache Auszeichnungssprache |
| 🎯 Wozu dient das? | Markdown ermöglicht das einfache Schreiben strukturierter Dokumente, die automatisch formatiert dargestellt werden können. |
| 🧠 Merksatz | **Markdown beschreibt Dokumente – nicht Programme.** |

<details>
<summary>💡 Beispiel</summary>

Aus

```markdown
# Überschrift

**Fett**
```

wird nach dem Rendern eine formatierte Überschrift mit fettem Text.

</details>

<details>
<summary>📚 Mehr wissen</summary>

Markdown wird unter anderem von GitHub, Obsidian, GitLab und vielen Dokumentationssystemen verwendet.

</details>

<details>
<summary>⚙️ Technischer Hintergrund</summary>

Markdown wird durch einen sogenannten Renderer in HTML umgewandelt.

Anschliessend stellt der Browser das HTML dar.

</details>

<details>
<summary>💼 Mein Arbeitsalltag</summary>

Für dein Babs-Wiki schreibst du alle Dokumentationen in Markdown.

GitHub rendert daraus automatisch schön formatierte Seiten.

</details>

<details>
<summary>🔗 Siehe auch</summary>

- HTML
- Rendern
- GitHub
- Obsidian

</details>

### Mapping

| Bereich | Inhalt |
|---|---|
| 🇬🇧 Englisch | Mapping |
| 🇩🇪 Deutsch | Zuordnung / Abbildung |
| 🎯 Wozu dient das? | Mapping ordnet Datenfelder oder Werte aus einem System den passenden Feldern oder Werten eines anderen Systems zu. |
| 🧠 Merksatz | **Mapping legt fest, welcher Wert wohin gehört.** |

<details>
<summary>💡 Beispiel</summary>

Zwei Systeme verwenden unterschiedliche Feldnamen:

| Quellsystem | Zielsystem |
|---|---|
| `VORNAME` | `firstName` |
| `NACHNAME` | `lastName` |
| `GEB_DAT` | `dateOfBirth` |

Das Mapping legt fest, dass beispielsweise der Wert aus `VORNAME` im Zielsystem in das Feld `firstName` geschrieben wird.

</details>

<details>
<summary>📚 Mehr wissen</summary>

Mapping kann verschiedene Arten von Zuordnungen enthalten:

- Feld zu Feld
- Wert zu Wert
- Datenformat zu Datenformat
- Quellsystem zu Zielsystem
- interner Code zu verständlicher Bezeichnung

Beispiel einer Wertzuordnung:

| Quellwert | Zielwert |
|---|---|
| `M` | `männlich` |
| `W` | `weiblich` |
| `U` | `unbekannt` |

</details>

<details>
<summary>⚙️ Technischer Hintergrund</summary>

Beim Mapping können Daten zusätzlich verändert werden.

Beispiele:

- Datumsformat umwandeln
- mehrere Felder zusammenführen
- einen Wert aufteilen
- Codes übersetzen
- leere Werte ersetzen
- Pflichtfelder prüfen

Ein fehlerhaftes Mapping kann dazu führen, dass Daten im falschen Feld landen oder vom Zielsystem nicht verarbeitet werden können.

</details>

<details>
<summary>💼 Mein Arbeitsalltag</summary>

Bei Tests kann ich prüfen:

- Werden alle Felder richtig zugeordnet?
- Stimmen Quell- und Zielwerte überein?
- Werden Datums- und Zahlenformate korrekt umgewandelt?
- Werden leere oder ungültige Werte richtig behandelt?
- Fehlen Pflichtfelder?
- Werden Codes korrekt übersetzt?

</details>

<details>
<summary>🔗 Siehe auch</summary>

- [Webservice](W.md#webservice)
- [XML](X.md#xml)
- Schnittstelle
- Datenformat

</details>