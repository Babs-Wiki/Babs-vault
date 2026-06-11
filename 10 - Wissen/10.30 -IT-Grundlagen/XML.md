
## Definition

XML (Extensible Markup Language) ist ein Format zur strukturierten Speicherung und Übertragung von Daten.

XML wird häufig verwendet, damit Systeme Informationen über APIs und Webservices austauschen können.

Siehe auch: [[API]]  
Siehe auch: [[Webservice]]

---

## Wichtigste XML-Bausteine

|Element|Beispiel|Bedeutung|
|---|---|---|
|Tag|`<Name>`|Kennzeichnet ein Datenfeld|
|Öffnender Tag|`<Name>`|Beginn eines Elements|
|Schliessender Tag|`</Name>`|Ende eines Elements|
|Inhalt|`Müller`|Der eigentliche Wert|
|Element|`<Name>Müller</Name>`|Komplettes Datenelement|
|Attribut|`<Person ID="123">`|Zusätzliche Information|
|Verschachtelung|`<Person><Name>Müller</Name></Person>`|Elemente können ineinander liegen|

---

## Einfaches Beispiel

```xml
<Person>
    <Name>Müller</Name>
    <Vorname>Max</Vorname>
</Person>
```

Bedeutung:

- Person
    
    - Name = Müller
        
    - Vorname = Max
        

---

## Beispiel mit Attribut

```xml
<Person ID="12345">
    <Name>Müller</Name>
</Person>
```

Hier besitzt die Person zusätzlich die ID 12345.

---

## Typische Fehler

### Fehlender schliessender Tag

Falsch:

```xml
<Name>Müller
```

Richtig:

```xml
<Name>Müller</Name>
```

---

### Falsche Verschachtelung

Falsch:

```xml
<Person>
    <Name>Müller
</Person>
</Name>
```

Richtig:

```xml
<Person>
    <Name>Müller</Name>
</Person>
```

---

## Merksatz

XML ist die Verpackung der Daten.

API = Die Regeln

XML = Die Daten

Webservice = Der Vermittler