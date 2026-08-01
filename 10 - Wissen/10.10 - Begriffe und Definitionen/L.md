- [LEFT JOIN](#left-join)

### LEFT JOIN

| Begriff | Deutsch | Merksatz |
|----------|---------|----------|
| **LEFT JOIN** | Verknüpfung zweier Datenbanktabellen | **Beim LEFT JOIN bleiben alle Datensätze der linken Tabelle erhalten.** |

Ein LEFT JOIN verbindet zwei Datenbanktabellen miteinander.

Alle Datensätze aus der linken Tabelle werden angezeigt – auch dann, wenn in der rechten Tabelle kein passender Datensatz vorhanden ist.

<details>
<summary>💡 Beispiel</summary>

Es gibt eine Tabelle mit Personen und eine Tabelle mit Telefonnummern.

Auch Personen ohne gespeicherte Telefonnummer sollen angezeigt werden.

```sql
SELECT Person.Name, Telefon.Nummer
FROM Person
LEFT JOIN Telefon
  ON Person.ID = Telefon.PersonID;
```

Alle Personen erscheinen im Ergebnis. Fehlt eine Telefonnummer, bleibt das entsprechende Feld leer.

</details>

<details>
<summary>📚 Mehr Wissen</summary>

Die linke Tabelle ist die Tabelle, die im SQL-Befehl zuerst genannt wird.

Ein LEFT JOIN ist hilfreich, wenn man auch Datensätze finden möchte, für die noch keine zugehörigen Informationen vorhanden sind.

Beispiel:

- alle Personen, auch ohne Adresse
- alle Tickets, auch ohne zuständige Person
- alle Produkte, auch ohne Bestellung

</details>

<details>
<summary>⚙️ Technik</summary>

Wenn in der rechten Tabelle kein passender Datensatz vorhanden ist, enthalten deren Felder den Wert `NULL`.

Die Verknüpfung erfolgt normalerweise über gemeinsame Schlüssel, beispielsweise:

- Personen-ID
- Ticket-ID
- Produkt-ID

Ein **INNER JOIN** würde dagegen nur Datensätze anzeigen, für die auf beiden Seiten eine passende Verbindung vorhanden ist.

</details>