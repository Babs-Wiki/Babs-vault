
## Begriffe

- [Redis](#redis)
- [Regedit](#regedit)
- [Registry](#registry)
- [Rendern](#rendern)
- [Rollbackmechanismus](#rollbackmechanismus)


# Rendern

| Bereich | Inhalt |
|---|---|
| 🇬🇧 Englisch | Render / Rendering |
| 🇩🇪 Deutsch | Darstellen, anzeigen, aufbereiten |
| 🎯 Wozu dient das? | Ein Programm wandelt Daten oder Code in eine sichtbare Darstellung um. |
| 🧠 Merksatz | **Rendern = Aus Code wird etwas Sichtbares.** |

<details>
<summary>💡 Beispiel</summary>

GitHub rendert deine Markdown-Datei.

Aus

```markdown
# API

**Hallo**
```

wird eine schön formatierte Webseite mit einer Überschrift und fettem Text.

</details>

<details>
<summary>📚 Mehr wissen</summary>

Nicht nur Webseiten werden gerendert.

Auch Spiele rendern 3D-Grafiken.

Videos werden gerendert.

PDFs werden gerendert.

Überall bedeutet es:

**Daten werden in eine sichtbare Form umgewandelt.**

</details>

<details>
<summary>⚙️ Technischer Hintergrund</summary>

Markdown selbst sieht nur wie Text aus.

Der Renderer liest den Markdown-Code und erzeugt daraus HTML.

Der Browser rendert anschließend das HTML und zeigt die fertige Seite an.

</details>

<details>
<summary>💼 Mein Arbeitsalltag</summary>

Wenn eine Markdown-Datei in GitHub schön formatiert erscheint, wurde sie erfolgreich gerendert.

Wenn etwas falsch dargestellt wird, spricht man oft von einem Rendering-Problem.

</details>

<details>
<summary>🔗 Siehe auch</summary>

- Markdown
- HTML
- Browser
- DOM (später)
- CSS (später)

</details>

### Redis

| Begriff | Deutsch | Merksatz |
|----------|---------|----------|
| **Redis** | In-Memory-Datenbank / Zwischenspeicher | **Redis hält Daten im Arbeitsspeicher und kann sie deshalb besonders schnell bereitstellen.** |

Redis ist eine sehr schnelle Datenbank, die Daten hauptsächlich im Arbeitsspeicher, also im RAM, speichert.

<details>
<summary>💡 Beispiel</summary>

Eine Anwendung benötigt immer wieder dieselben Stammdaten.

Statt diese jedes Mal aus der eigentlichen Datenbank zu laden, werden sie vorübergehend in Redis gespeichert und können schneller abgerufen werden.

</details>

<details>
<summary>📚 Mehr Wissen</summary>

Redis wird häufig als Cache, Session-Speicher oder für Warteschlangen verwendet.

Ein Cache ist ein schneller Zwischenspeicher für Daten, die oft benötigt werden.

</details>

<details>
<summary>⚙️ Technik</summary>

Redis ist eine NoSQL-Datenbank und unterstützt unter anderem:

- Texte und Zahlen
- Listen
- Mengen
- Schlüssel-Wert-Paare
- Warteschlangen

Die Daten können zusätzlich auf einem dauerhaften Speicher gesichert werden.

</details>

### Rollbackmechanismus

| Bereich | Inhalt |
|---|---|
| 🇬🇧 Englisch | Rollback mechanism |
| 🇩🇪 Deutsch | Rücksetzmechanismus |
| 🎯 Wozu dient das? | Ein Rollbackmechanismus macht bereits ausgeführte Änderungen rückgängig, wenn ein Vorgang nicht erfolgreich abgeschlossen werden kann. Dadurch bleibt das System in einem stabilen und konsistenten Zustand. |
| 🧠 Merksatz | **Wenn etwas schiefgeht, setzt der Rollback die Änderungen zurück.** |

<details>
<summary>💡 Beispiel</summary>

Ein System soll zehn Datensätze ändern.

Nach dem siebten Datensatz tritt ein Fehler auf.

**Ohne Rollback:**

- sieben Datensätze wurden geändert
- drei Datensätze wurden nicht geändert
- der Datenbestand ist inkonsistent

**Mit Rollback:**

- die sieben Änderungen werden zurückgenommen
- alle Datensätze befinden sich wieder im ursprünglichen Zustand
- das System bleibt konsistent

</details>

<details>
<summary>📚 Mehr wissen</summary>

Ein Rollback ist besonders wichtig bei Vorgängen, die aus mehreren zusammengehörenden Schritten bestehen.

Typische Einsatzbereiche sind:

- Datenbankänderungen
- Webservice-Verarbeitungen
- Datenimporte
- Softwareupdates
- Konfigurationsänderungen

Das Gegenteil eines Rollbacks ist häufig ein **Commit**. Ein Commit bestätigt, dass alle Änderungen erfolgreich waren und dauerhaft gespeichert werden dürfen.

</details>

<details>
<summary>⚙️ Technischer Hintergrund</summary>

In einer Datenbank werden mehrere zusammengehörende Änderungen häufig innerhalb einer **Transaktion** ausgeführt.

Am Ende gibt es vereinfacht zwei Möglichkeiten:

- **Commit:** Alle Änderungen werden endgültig gespeichert.
- **Rollback:** Alle Änderungen der Transaktion werden zurückgenommen.

Ein Rollback funktioniert nur zuverlässig, wenn das System weiss:

- welche Änderungen ausgeführt wurden
- welche Änderungen zurückgenommen werden können
- welcher stabile Zustand wiederhergestellt werden soll

</details>

<details>
<summary>💼 Mein Arbeitsalltag</summary>

Bei Tests kann ich prüfen:

- Was geschieht, wenn während einer Verarbeitung ein Fehler auftritt?
- Werden bereits ausgeführte Änderungen zurückgenommen?
- Bleiben teilweise veränderte Datensätze zurück?
- Wird eine verständliche Fehlermeldung ausgegeben?
- Wird der Rollback in einem Log dokumentiert?
- Bleibt der Datenbestand nach dem Fehler konsistent?

</details>

<details>
<summary>🔗 Siehe auch</summary>

- [API](A.md#api)
- [Webservice](W.md#webservice)
- [XML](X.md#xml)

</details>

<details>
<summary>📖 Vertiefung</summary>

- [Rollbackmechanismus – ausführliche Erklärung](<../10.60 - Vertiefungsseiten/Rollbackmechanismus.md>)

</details>

### Regedit

| Bereich | Inhalt |
|---|---|
| 🇬🇧 Englisch | Registry Editor |
| 🇩🇪 Deutsch | Registrierungs-Editor |
| 🎯 Wozu dient das? | Regedit dient zum Anzeigen, Suchen und Bearbeiten von Einstellungen in der Windows-Registry. |
| 🧠 Merksatz | **Regedit ist das Werkzeug zum Bearbeiten der Windows-Registry.** |

<details>
<summary>💡 Beispiel</summary>

Eine Herstelleranleitung verlangt, einen bestimmten Windows-Eintrag zu kontrollieren.

Regedit wird geöffnet und der angegebene Registry-Pfad aufgerufen. Dort kann geprüft werden, ob der erwartete Wert vorhanden und korrekt eingetragen ist.

</details>

<details>
<summary>📚 Mehr wissen</summary>

Regedit ist bereits in Windows enthalten.

Das Werkzeug kann über den Ausführen-Dialog gestartet werden:

```text
Win + R
```

Danach:

```text
regedit
```

Änderungen können sofort Auswirkungen auf Windows oder installierte Programme haben.

</details>

<details>
<summary>⚙️ Technischer Hintergrund</summary>

Regedit stellt die Registry als Baumstruktur dar.

Sie besteht aus:

- Hauptbereichen
- Schlüsseln
- Unterschlüsseln
- Werten
- Wertdaten

Vor einer Änderung kann ein Registry-Schlüssel als `.reg`-Datei exportiert werden.

</details>

<details>
<summary>💼 Mein Arbeitsalltag</summary>

Regedit kann mir bei der Fehleranalyse oder beim Umsetzen einer dokumentierten Herstelleranleitung begegnen.

Dabei prüfe ich genau:

- den vollständigen Registry-Pfad
- den Namen des Wertes
- den Werttyp
- die vorhandenen Wertdaten
- die benötigten Berechtigungen

Unbekannte Registry-Einträge ändere ich nicht ohne klare Anleitung.

</details>

<details>
<summary>🔗 Siehe auch</summary>

- [Registry](#registry)

</details>

<details>
<summary>📖 Vertiefung</summary>

- [Regedit – ausführliche Erklärung](<../10.50 - Tools & Programme/Regedit.md>)

</details>

### Registry

| Bereich | Inhalt |
|---|---|
| 🇬🇧 Englisch | Windows Registry |
| 🇩🇪 Deutsch | Windows-Registrierungsdatenbank |
| 🎯 Wozu dient das? | Die Registry speichert zentrale Einstellungen von Windows, Benutzerkonten, Hardware und vielen installierten Programmen. |
| 🧠 Merksatz | **Die Registry ist die zentrale Konfigurationsdatenbank von Windows.** |

<details>
<summary>💡 Beispiel</summary>

Ein Programm speichert in der Registry:

- seinen Installationspfad
- bestimmte Programmeinstellungen
- Informationen zur installierten Version

Beim Start kann das Programm diese Werte auslesen und verwenden.

</details>

<details>
<summary>📚 Mehr wissen</summary>

Die Registry enthält unter anderem:

- Windows-Einstellungen
- Benutzerprofile
- Hardware-Konfigurationen
- Programmeinstellungen
- Dateizuordnungen
- Sicherheits- und Systemeinstellungen

Sie ist hierarchisch aufgebaut und ähnelt einer Ordnerstruktur.

</details>

<details>
<summary>⚙️ Technischer Hintergrund</summary>

Die Registry besteht aus Schlüsseln und Werten.

Wichtige Hauptbereiche sind:

- `HKEY_LOCAL_MACHINE` – Einstellungen für den gesamten Computer
- `HKEY_CURRENT_USER` – Einstellungen des aktuell angemeldeten Benutzers
- `HKEY_USERS` – Einstellungen verschiedener Benutzerprofile
- `HKEY_CLASSES_ROOT` – Dateizuordnungen und Programmverknüpfungen
- `HKEY_CURRENT_CONFIG` – aktuelle Hardwarekonfiguration

Die Registry kann mit Regedit angezeigt und bearbeitet werden.

</details>

<details>
<summary>💼 Mein Arbeitsalltag</summary>

Die Registry kann bei der Analyse von Windows- oder Programmproblemen eine Rolle spielen.

Dabei kann geprüft werden:

- ob ein erwarteter Schlüssel vorhanden ist
- ob ein Wert korrekt gesetzt wurde
- ob eine Konfiguration für den Benutzer oder den ganzen Computer gilt
- ob eine Herstelleranleitung richtig umgesetzt wurde

Änderungen erfolgen nur kontrolliert und nach Möglichkeit mit vorheriger Sicherung.

</details>

<details>
<summary>🔗 Siehe auch</summary>

- [Regedit](#regedit)

</details>

<details>
<summary>📖 Vertiefung</summary>

- [Regedit und Windows-Registry – ausführliche Erklärung](<../10.50 - Tools & Programme/Regedit.md>)

</details>