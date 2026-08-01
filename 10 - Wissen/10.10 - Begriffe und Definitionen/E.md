
- [Ereignisanzeige (Event Viewer)](#ereignisanzeige-event-viewer)

### Ereignisanzeige (Event Viewer)

| Bereich | Inhalt |
|---|---|
| 🇬🇧 Englisch | Event Viewer |
| 🇩🇪 Deutsch | Ereignisanzeige |
| 🎯 Wozu dient das? | Die Ereignisanzeige zeigt protokollierte Meldungen, Warnungen und Fehler von Windows, Programmen und Diensten. Sie hilft bei der Suche nach der Ursache eines Problems. |
| 🧠 Merksatz | **Die Ereignisanzeige zeigt, was Windows und Programme zu einem bestimmten Zeitpunkt protokolliert haben.** |

<details>
<summary>💡 Beispiel</summary>

Eine Anwendung stürzt um `10:15 Uhr` ab.

In der Ereignisanzeige wird unter **Windows-Protokolle → Anwendung** nach Fehlern aus diesem Zeitraum gesucht.

Ein passendes Ereignis kann Hinweise auf das betroffene Programm, ein fehlerhaftes Modul oder eine andere mögliche Ursache enthalten.

</details>

<details>
<summary>📚 Mehr wissen</summary>

Die Ereignisanzeige kann unter anderem Informationen enthalten über:

- Programmfehler
- Windows-Fehler
- Warnungen
- Start- und Herunterfahrvorgänge
- Anmeldeversuche
- Dienste
- Installationen
- Sicherheitsereignisse

Sie zeigt nur Ereignisse, die tatsächlich protokolliert wurden.

Nicht jedes angezeigte Ereignis ist automatisch die Ursache eines Problems.

</details>

<details>
<summary>⚙️ Technischer Hintergrund</summary>

Ein Ereignis enthält normalerweise Angaben wie:

- Datum und Uhrzeit
- Quelle
- Ereignis-ID
- Ereignisstufe
- Benutzer
- Computer
- Beschreibung
- technische Details

Wichtige Windows-Protokolle sind:

- Anwendung
- Sicherheit
- Installation
- System

Die Ereignisanzeige kann über den Ausführen-Dialog gestartet werden:

```text
Win + R
```

Danach:

```text
eventvwr.msc
```

</details>

<details>
<summary>💼 Mein Arbeitsalltag</summary>

Bei einer Fehleranalyse kann ich:

1. den Zeitpunkt des Problems notieren
2. das passende Protokoll öffnen
3. nach Fehlern oder Warnungen suchen
4. Quelle und Ereignis-ID prüfen
5. die Beschreibung lesen
6. kontrollieren, ob das Ereignis zum beobachteten Problem passt

Relevante Angaben können anschliessend für ein Ticket oder eine Rückfrage dokumentiert werden.

</details>

<details>
<summary>🔗 Siehe auch</summary>

- [Regedit](R.md#regedit)

</details>

<details>
<summary>📖 Vertiefung</summary>

- [Windows-Ereignisanzeige – ausführliche Erklärung](<../10.50 - Tools & Programme/Windows – Ereignisanzeige.md>)

</details>