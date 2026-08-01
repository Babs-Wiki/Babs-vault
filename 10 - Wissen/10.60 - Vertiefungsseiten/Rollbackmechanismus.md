

Ein **Rollbackmechanismus** setzt bereits ausgeführte Änderungen zurück, wenn während eines Vorgangs ein Fehler auftritt.

> **Merksatz:** Wenn etwas schiefgeht, versetzt der Rollback das System in den letzten stabilen Zustand zurück.

---

<details>
<summary>📖 Definition</summary>

Ein Rollbackmechanismus macht Änderungen rückgängig, wenn ein Prozess nicht vollständig oder fehlerfrei abgeschlossen werden kann.

Das System kehrt dabei möglichst zum letzten stabilen Zustand zurück.

Dadurch sollen folgende Probleme verhindert werden:

- unvollständige Änderungen
- inkonsistente Daten
- beschädigte Systemzustände
- Datenverlust
- nur teilweise ausgeführte Vorgänge

</details>

<details>
<summary>💡 Einfach erklärt</summary>

Stell dir vor, ein System soll zehn Datensätze ändern.

Nach dem siebten Datensatz tritt ein Fehler auf.

### Ohne Rollback

- sieben Datensätze wurden geändert
- drei Datensätze wurden nicht geändert
- der Datenbestand ist nicht mehr einheitlich

### Mit Rollback

- die sieben bereits ausgeführten Änderungen werden zurückgenommen
- alle zehn Datensätze befinden sich wieder im ursprünglichen Zustand
- das System bleibt konsistent

> **Rollback bedeutet:** Entweder wird der ganze Vorgang erfolgreich abgeschlossen oder die Änderungen werden zurückgenommen.

</details>

<details>
<summary>🌐 Beispiel im Webservice</summary>

Ein Webservice startet eine Verarbeitung:

```text
Webservice nimmt Anfrage entgegen
              ↓
Daten werden geprüft
              ↓
Daten werden geändert
              ↓
Fehler tritt auf
              ↓
Rollback wird ausgelöst
              ↓
Änderungen werden rückgängig gemacht
```

Dadurch bleibt der ursprüngliche Datenbestand erhalten.

Ohne Rollback könnten einzelne Daten bereits verändert worden sein, obwohl die gesamte Anfrage nicht erfolgreich abgeschlossen wurde.

</details>

<details>
<summary>🗄️ Beispiel in einer Datenbank</summary>

Bei einer Überweisung müssen zwei Änderungen ausgeführt werden:

```text
Konto A: −100 CHF
Konto B: +100 CHF
```

Tritt zwischen diesen beiden Schritten ein Fehler auf, könnte ohne Rollback Folgendes passieren:

- Konto A wurden 100 CHF abgezogen
- Konto B hat die 100 CHF nicht erhalten

Mit einem Rollback wird auch die Abbuchung von Konto A zurückgenommen.

Der ursprüngliche Zustand wird wiederhergestellt und das Geld geht nicht verloren.

</details>

<details>
<summary>🔄 Beispiel bei einem Update</summary>

Ein Systemupdate wird installiert.

Während der Installation tritt ein Fehler auf.

Der Rollbackmechanismus kann dann:

- bereits installierte Änderungen entfernen
- neue Dateien zurücksetzen
- die vorherige Konfiguration wiederherstellen
- die letzte funktionierende Softwareversion aktivieren

So soll verhindert werden, dass das System nach einem fehlgeschlagenen Update nicht mehr funktioniert.

</details>

<details>
<summary>🎯 Warum ist ein Rollback wichtig?</summary>

Ein Rollback schützt Systeme und Daten vor fehlerhaften oder unvollständigen Änderungen.

Er hilft dabei:

- Daten konsistent zu halten
- halbfertige Vorgänge zu verhindern
- Fehler kontrolliert zu behandeln
- einen stabilen Zustand wiederherzustellen
- Risiken bei Änderungen und Updates zu reduzieren

Besonders wichtig ist ein Rollback bei Vorgängen, die aus mehreren voneinander abhängigen Schritten bestehen.

</details>

<details>
<summary>⚙️ Technischer Hintergrund</summary>

In Datenbanken werden mehrere zusammengehörende Änderungen häufig innerhalb einer **Transaktion** ausgeführt.

Eine Transaktion kann normalerweise auf zwei Arten beendet werden:

- **Commit:** Alle Änderungen werden endgültig gespeichert.
- **Rollback:** Alle Änderungen der Transaktion werden zurückgenommen.

Vereinfacht:

```text
Transaktion beginnt
        ↓
Änderungen werden ausgeführt
        ↓
   War alles erfolgreich?
       ↙           ↘
     Ja             Nein
      ↓               ↓
   Commit          Rollback
      ↓               ↓
Änderungen       Änderungen
speichern        zurücknehmen
```

Ein Rollback funktioniert allerdings nur dann zuverlässig, wenn das System vorher festgelegt hat, welche Änderungen zurückgenommen werden können und welcher Zustand wiederhergestellt werden soll.

</details>

<details>
<summary>🔗 Zusammenhang mit anderen Begriffen</summary>

Bei einer Verarbeitung können mehrere Bestandteile zusammenspielen:

```text
API
↓
definiert die Regeln der Kommunikation

XML
↓
enthält oder überträgt die Daten

Webservice
↓
nimmt die Anfrage entgegen und verarbeitet sie

Fehler
↓
Verarbeitung kann nicht abgeschlossen werden

Rollback
↓
bereits ausgeführte Änderungen werden zurückgenommen
```

Der Rollback ist damit häufig ein Sicherheitsmechanismus innerhalb eines grösseren Prozesses.

</details>

<details>
<summary>💼 Mein Arbeitsalltag</summary>

Ein Rollbackmechanismus kann mir bei Tests von Webservices, Datenänderungen oder Updates begegnen.

Dabei kann wichtig sein zu prüfen:

- Was geschieht, wenn während der Verarbeitung ein Fehler auftritt?
- Werden bereits ausgeführte Änderungen zurückgenommen?
- Bleiben teilweise veränderte Datensätze zurück?
- Wird eine verständliche Fehlermeldung ausgegeben?
- Kann der ursprüngliche Zustand vollständig wiederhergestellt werden?
- Wird der Rollback im Log oder in der Ereignisanzeige dokumentiert?

Besonders wichtig ist die Prüfung, ob das System nach einem Fehler weiterhin einen konsistenten Datenbestand besitzt.

</details>

<details>
<summary>🔗 Siehe auch</summary>

- [API](<../10.10 - Glossar/A.md#api>)
- [XML](<../10.10 - Glossar/X.md#xml>)
- [Webservice](<../10.10 - Glossar/W.md#webservice>)
- Commit
- Transaktion

</details>