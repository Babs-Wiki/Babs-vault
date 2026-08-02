

GitHub ist die zentrale Online-Ablage für mein **Babs-Wiki**.  
Es ist mein Referenzsystem: Was auf GitHub korrekt dargestellt wird, gilt als massgebend.

---

## Wofür nutze ich GitHub?

- Zugriff auf mein Wiki im Büro über den Browser
- Bearbeiten von Markdown-Dateien ohne installiertes Obsidian
- Speichern und Nachverfolgen von Änderungen
- Synchronisation zwischen Büro, Handy und Obsidian zu Hause
- Kontrolle, ob Links und einklappbare Bereiche korrekt funktionieren

---

## Mein Arbeitsablauf zu Hause

Wenn ich zuvor im Büro oder auf dem Handy etwas geändert habe:

1. Obsidian öffnen
2. Zuerst **Pull** ausführen
3. Dateien bearbeiten
4. Änderungen speichern
5. **Commit** erstellen
6. **Push** ausführen
7. Auf GitHub kontrollieren

> [!important]
> Zuerst **Pull**, danach bearbeiten.  
> Am Schluss **Commit und Push**.

---

## Mein Arbeitsablauf im Büro

1. GitHub im Browser öffnen
2. Gewünschte Markdown-Datei auswählen
3. Datei bearbeiten
4. Änderungen mit einem Commit speichern
5. Zu Hause vor der nächsten Bearbeitung zuerst einen Pull durchführen

---

## Mein Arbeitsablauf auf dem Handy

Auf dem Handy kann ich:

- Dateien lesen
- nach Begriffen suchen
- kleine Änderungen vornehmen
- neue Inhalte kontrollieren

Änderungen vom Handy werden beim nächsten **Pull** nach Obsidian übernommen.

---

## Die wichtigsten Begriffe

### Pull

Ein Pull lädt die neusten Änderungen von GitHub auf mein Gerät herunter.

**Merksatz:**  
Pull = Änderungen zu mir holen.

### Commit

Ein Commit speichert einen bestimmten Änderungsstand mit einer kurzen Beschreibung.

**Merksatz:**  
Commit = Änderung festhalten.

### Push

Ein Push überträgt meine lokalen Änderungen zu GitHub.

**Merksatz:**  
Push = Änderungen zu GitHub schicken.

---

## Die richtige Reihenfolge

```text
Änderungen auf GitHub vorhanden
            ↓
           Pull
            ↓
      In Obsidian arbeiten
            ↓
          Commit
            ↓
           Push
            ↓
   Auf GitHub kontrollieren
```

---

## Wichtige Hinweise für mein Wiki

### Links

Normale Markdown-Links funktionieren sowohl in GitHub als auch in Obsidian:

```markdown
[Backend](B.md#backend)
```

Bei Dateien in einem anderen Ordner:

```markdown
[Windows-Ereignisanzeige](<../10.50 - Tools & Programme/Windows - Ereignisanzeige.md>)
```

Dateinamen und Pfade müssen exakt stimmen. Auch ein anderer Bindestrich kann dazu führen, dass ein Link nicht funktioniert.

### Einklappbare Bereiche

Für einklappbare Inhalte verwende ich:

```html
<details>
<summary>📚 Mehr wissen</summary>

Inhalt

</details>
```

Diese Darstellung funktioniert zuverlässig auf GitHub und in der Obsidian-Leseansicht.

---

## Häufige Fehler

### Änderung fehlt in Obsidian

Mögliche Ursache:

- Pull wurde noch nicht ausgeführt.

### Änderung fehlt auf GitHub

Mögliche Ursachen:

- Commit wurde nicht erstellt.
- Push wurde nicht ausgeführt.

### Link funktioniert nicht

Prüfen:

- Stimmt der Dateiname?
- Stimmt der Ordner?
- Stimmt die Überschrift nach dem `#`?
- Wurde ein normaler Bindestrich `-` oder ein Gedankenstrich `–` verwendet?
- Enthält der Pfad Leerzeichen oder Sonderzeichen?

---

## Siehe auch

-[HTML](h.md#thml)
-[Rendern](r.md#rendern)
