
- [Query](#query)

### Query

| Bereich | Inhalt |
|---|---|
| 🇬🇧 Englisch | Query |
| 🇩🇪 Deutsch | Abfrage |
| 🎯 Wozu dient das? | Eine Query sucht, filtert oder verändert gezielt Daten in einer Datenbank oder einem anderen Datenbestand. |
| 🧠 Merksatz | **Eine Query ist eine gezielte Frage an die Daten.** |

<details>
<summary>💡 Beispiel</summary>

Eine Anwendung sucht alle Orte, die mit `Thu` beginnen.

Vereinfacht könnte die Query so aussehen:

```sql
SELECT Ort
FROM Ortschaften
WHERE Ort LIKE 'Thu%';
```

Die Datenbank liefert beispielsweise folgende Treffer:

```text
Thun
Thunstetten
Thurnen
```

</details>

<details>
<summary>📚 Mehr wissen</summary>

Eine Query kann beispielsweise:

- Daten suchen
- Ergebnisse filtern
- Daten sortieren
- Tabellen miteinander verbinden
- neue Daten speichern
- bestehende Daten ändern
- Daten löschen

Im normalen Sprachgebrauch ist mit Query häufig eine Such- oder Datenbankabfrage gemeint.

</details>

<details>
<summary>⚙️ Technischer Hintergrund</summary>

Relationale Datenbanken verwenden häufig SQL für Queries.

Typische SQL-Befehle sind:

| Befehl | Funktion |
|---|---|
| `SELECT` | Daten lesen |
| `INSERT` | neue Daten einfügen |
| `UPDATE` | bestehende Daten ändern |
| `DELETE` | Daten löschen |

Filter werden häufig mit `WHERE` festgelegt.

Beispiel:

```sql
SELECT *
FROM Person
WHERE Ort = 'Thun';
```

Diese Query sucht alle Personen mit dem Ort `Thun`.

</details>

<details>
<summary>💼 Mein Arbeitsalltag</summary>

Eine Query begegnet mir beispielsweise, wenn eine Suchhilfe oder Fachanwendung bestimmte Daten anfordert.

Bei Tests kann ich prüfen:

- Werden die richtigen Suchkriterien verwendet?
- Liefert die Abfrage die erwarteten Treffer?
- Werden zu viele oder zu wenige Daten angezeigt?
- Funktionieren mehrere Filter gemeinsam?
- Werden leere oder ungültige Eingaben korrekt behandelt?
- Ist die Abfrage performant?

</details>

<details>
<summary>🔗 Siehe auch</summary>

- [Datenbank](D.md#datenbank)
- [LEFT JOIN](L.md#left-join)
- [Performant und inperformant](P.md#performant-und-inperformant)
- [SQL](s.md#sql)

</details>