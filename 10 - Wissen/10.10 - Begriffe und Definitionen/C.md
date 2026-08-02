- [Cache](#cache)
- [CSS](#css)

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

## CSS

| Feld | Inhalt |
|------|--------|
| 🇬🇧 **Englisch** | Cascading Style Sheets |
| 🇩🇪 **Deutsch** | Kaskadierende Formatvorlagen |
| 🎯 **Wozu dient das?** | CSS bestimmt das Aussehen und die Anordnung von HTML-Elementen, zum Beispiel Farben, Abstände, Schriftgrössen und Positionen. |
| 🧠 **Merksatz** | **HTML baut die Webseite auf – CSS gestaltet sie.** |

<details>
<summary>💡 Beispiel</summary>

HTML erstellt einen Textabschnitt:

```html
<p>Hallo Babs</p>
```

CSS bestimmt dessen Aussehen:

```css
p {
  font-size: 18px;
  font-weight: bold;
}
```

Dadurch wird der Text grösser und fett dargestellt.

</details>

<details>
<summary>📚 Mehr wissen</summary>

Mit CSS können unter anderem festgelegt werden:

- Schriftart und Schriftgrösse,
- Farben,
- Abstände,
- Rahmen,
- Breite und Höhe,
- Positionen,
- Anordnungen von Elementen,
- Darstellung auf unterschiedlichen Bildschirmgrössen.

CSS verändert normalerweise nicht den Inhalt einer Webseite, sondern dessen Darstellung.

</details>

<details>
<summary>⚙️ Technischer Hintergrund</summary>

Eine CSS-Regel besteht meistens aus:

```css
p {
  font-size: 18px;
}
```

- `p` ist der **Selektor**. Er bestimmt, welches Element angesprochen wird.
- `font-size` ist die **Eigenschaft**.
- `18px` ist der zugewiesene **Wert**.

Das Wort **Cascading** bedeutet, dass mehrere Gestaltungsregeln zusammenwirken können. Dabei entscheidet eine festgelegte Reihenfolge, welche Regel angewendet wird.

</details>

<details>
<summary>💼 Mein Arbeitsalltag</summary>

CSS begegnet mir bei Webseiten und webbasierten Benutzeroberflächen.

Darstellungsfehler wie falsche Abstände, verschobene Felder oder schlecht angeordnete Schaltflächen können mit CSS zusammenhängen.

</details>

<details>
<summary>🔗 Siehe auch</summary>

- [Browser](B.md#browser)
- [DOM](D.md#dom)
- [HTML](H.md#html)
- [Rendern](R.md#rendern)

</details>