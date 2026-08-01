- [Cache](#cache)

### Cache

| Bereich | Inhalt |
|---|---|
| 🇬🇧 Englisch | Cache |
| 🇩🇪 Deutsch | Zwischenspeicher |
| 🎯 Wozu dient das? | Häufig benötigte Daten werden vorübergehend gespeichert, damit sie schneller verfügbar sind und nicht jedes Mal neu geladen oder berechnet werden müssen. |
| 🧠 Merksatz | **Cache = schneller Zwischenspeicher.** |

<details>
<summary>💡 Beispiel</summary>

Eine Anwendung benötigt immer wieder dieselben Daten.

Beim ersten Aufruf werden die Daten aus der Datenbank geladen und zusätzlich im Cache gespeichert. Beim nächsten Aufruf können sie direkt aus dem Cache gelesen werden.

Dadurch reagiert die Anwendung schneller und die eigentliche Datenbank wird weniger belastet.

</details>

<details>
<summary>📚 Mehr wissen</summary>

Ein Cache bietet vor allem folgende Vorteile:

- schnellerer Zugriff auf häufig benötigte Daten
- kürzere Ladezeiten
- weniger Belastung für Datenbanken oder andere Systeme
- weniger wiederholte Berechnungen oder Datenübertragungen

Ein möglicher Nachteil ist, dass im Cache noch veraltete Daten liegen können.

Darum muss geregelt werden, wann Daten im Cache aktualisiert oder gelöscht werden.

</details>

<details>
<summary>⚙️ Technischer Hintergrund</summary>

Ein Cache kann sich an verschiedenen Stellen befinden, beispielsweise:

- im Browser
- in einer Anwendung
- auf einem Server
- zwischen einer Anwendung und einer Datenbank
- direkt im Arbeitsspeicher

Redis kann beispielsweise als Cache eingesetzt werden.

Wenn ein gesuchter Wert bereits im Cache vorhanden ist, spricht man von einem **Cache Hit**.

Fehlt der Wert und muss zuerst aus der ursprünglichen Quelle geladen werden, spricht man von einem **Cache Miss**.

</details>

<details>
<summary>🔗 Siehe auch</summary>

- [Puffer](P.md#puffer)
- [Redis](R.md#redis)

</details>