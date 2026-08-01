# Puffer

Ein **Puffer** speichert Daten kurzfristig zwischen, bis sie weiterverarbeitet werden können.

> **Merksatz:** Ein Puffer ist ein Wartebereich für Daten.

---

<details>
<summary>📖 Definition</summary>

Ein Puffer speichert Daten kurzfristig zwischen, bis sie weiterverarbeitet werden.

Er dient als Wartebereich und hilft dabei, dass Daten:

- nicht verloren gehen
- geordnet verarbeitet werden
- nicht alle gleichzeitig bearbeitet werden müssen
- unterschiedliche Verarbeitungsgeschwindigkeiten ausgeglichen werden

</details>

<details>
<summary>💡 Vergleich aus dem Alltag</summary>

Ein Puffer funktioniert ähnlich wie ein Wartezimmer beim Arzt:

```text
Patienten kommen an
        ↓
Wartezimmer – Puffer
        ↓
Behandlung nacheinander
        ↓
Fertig
```

Der Puffer sorgt dafür, dass nicht alle Personen gleichzeitig behandelt werden müssen.

</details>

<details>
<summary>🖨️ Beispiel: Druckaufträge</summary>

Mehrere Benutzerinnen und Benutzer senden gleichzeitig Druckaufträge.

```text
Benutzer
   ↓
Druckerwarteschlange – Puffer
   ↓
Drucker verarbeitet Auftrag für Auftrag
```

Die Druckaufträge warten im Puffer, bis der Drucker sie nacheinander bearbeiten kann.

</details>

<details>
<summary>🌐 Beispiel: Webservice-Anfragen</summary>

Mehrere Systeme senden gleichzeitig Anfragen an einen Webservice.

```text
System A ─┐
System B ─┼─→ Puffer → Webservice
System C ─┘
```

Der Puffer nimmt die Anfragen entgegen und hält sie bereit, bis sie verarbeitet werden können.

Beispielsweise:

1. System A sendet eine Anfrage.
2. System B sendet gleichzeitig eine weitere Anfrage.
3. System C sendet ebenfalls eine Anfrage.
4. Die Anfragen warten im Puffer.
5. Der Webservice verarbeitet sie entsprechend der vorgesehenen Reihenfolge oder Priorität.

</details>

<details>
<summary>📥 Beispiel: Datenimporte</summary>

Bei einem Datenimport treffen viele Datensätze ein.

```text
Datei
  ↓
Puffer
  ↓
Verarbeitung der Datensätze
```

Werden beispielsweise 1'000 Datensätze geliefert, kann das System sie im Puffer aufnehmen und schrittweise verarbeiten.

Dadurch muss nicht der gesamte Datenbestand gleichzeitig verarbeitet werden.

</details>

<details>
<summary>📋 Beispiel: Log-Daten</summary>

Systemereignisse entstehen laufend, beispielsweise:

- Fehler
- Warnungen
- Anmeldungen
- technische Statusmeldungen

Diese Informationen können zunächst in einem Puffer gesammelt und anschliessend gespeichert oder ausgewertet werden.

```text
Systemereignisse
       ↓
     Puffer
       ↓
Speicherung oder Auswertung
```

</details>

<details>
<summary>🔗 Unterschied zwischen Puffer und Cache</summary>

Ein Puffer und ein Cache speichern Daten vorübergehend, erfüllen aber unterschiedliche Aufgaben.

| Puffer | Cache |
|---|---|
| Daten warten auf ihre Verarbeitung. | Bereits bekannte Daten werden für einen schnelleren Zugriff gespeichert. |
| Gleicht unterschiedliche Verarbeitungsgeschwindigkeiten aus. | Verhindert unnötiges erneutes Laden oder Berechnen. |
| Beispiel: Druckerwarteschlange | Beispiel: zwischengespeicherte Datenbankabfrage |

> **Merksatz:**  
> **Puffer = Daten warten.**  
> **Cache = Daten schneller wiederverwenden.**

</details>

<details>
<summary>⚙️ Technischer Hintergrund</summary>

Ein Puffer kann sich im Arbeitsspeicher, in einer Datei oder in einem speziellen Warteschlangensystem befinden.

Je nach Anwendung kann die Verarbeitung erfolgen:

- in der Reihenfolge des Eingangs
- nach einer festgelegten Priorität
- in mehreren Verarbeitungsschritten
- durch einen Hintergrundprozess

Ist ein Puffer voll, muss das System festlegen, was geschieht. Beispielsweise können neue Daten abgewiesen, ältere Daten überschrieben oder weitere Speicherkapazitäten verwendet werden.

</details>

<details>
<summary>💼 Mein Arbeitsalltag</summary>

Ein Puffer kann mir begegnen, wenn Daten oder Anfragen nicht sofort verarbeitet werden.

Bei Tests kann beispielsweise wichtig sein:

- Werden alle Daten in den Puffer aufgenommen?
- Bleibt die richtige Reihenfolge erhalten?
- Gehen Anfragen verloren?
- Was passiert, wenn sehr viele Daten gleichzeitig eintreffen?
- Wird der Puffer nach der Verarbeitung korrekt geleert?
- Werden Fehler oder blockierte Einträge erkannt?

</details>

<details>
<summary>🔗 Siehe auch</summary>

- Cache
- Webservice
- Synchron und asynchron
- Warteschlange

</details>