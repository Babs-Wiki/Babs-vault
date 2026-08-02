## Begriffe

- [XML](#xml)

### XML

| Begriff | Deutsch | Merksatz |
|----------|---------|----------|
| **Extensible Markup Language (XML)** | Erweiterbare Auszeichnungssprache | **XML stellt Daten mit beschrifteten Elementen strukturiert dar.** |

XML ist ein Textformat, mit dem Daten strukturiert gespeichert und zwischen verschiedenen Systemen ausgetauscht werden können.

<details>
<summary>💡 Beispiel</summary>

```xml
<person>
  <vorname>Barbara</vorname>
  <nachname>Muster</nachname>
</person>
```

Die Bezeichnungen zwischen den spitzen Klammern beschreiben, welche Daten enthalten sind.

- `<person>` ist das übergeordnete Element.
- `<vorname>` enthält den Vornamen.
- `<nachname>` enthält den Nachnamen.

</details>

<details>
<summary>📚 Mehr Wissen</summary>

XML wird häufig für Schnittstellen, Konfigurationsdateien und den Datenaustausch zwischen verschiedenen Anwendungen verwendet.

Die Bezeichnung **erweiterbar** bedeutet, dass die verwendeten Elemente selbst definiert werden können. Es gibt also nicht nur fest vorgegebene Bezeichnungen.

XML ist für Menschen und Maschinen lesbar, benötigt aber meistens mehr Text als beispielsweise JSON.

</details>

<details>
<summary>⚙️ Technik</summary>

Ein XML-Dokument besteht aus Elementen beziehungsweise Tags.

Ein Element besitzt normalerweise einen öffnenden und einen schliessenden Tag:

```xml
<vorname>Barbara</vorname>
```

Der öffnende Tag lautet:

```xml
<vorname>
```

Der schliessende Tag enthält zusätzlich einen Schrägstrich:

```xml
</vorname>
```

Die Elemente müssen korrekt ineinander verschachtelt sein.

Richtig:

```xml
<person>
  <vorname>Barbara</vorname>
</person>
```

Falsch:

```xml
<person>
  <vorname>Barbara
</person>
  </vorname>
```

Ein XML-Dokument darf nur ein übergeordnetes Wurzelelement besitzen.

XML unterscheidet ausserdem zwischen Gross- und Kleinschreibung. `<Name>` und `<name>` gelten deshalb als unterschiedliche Elemente.

</details>