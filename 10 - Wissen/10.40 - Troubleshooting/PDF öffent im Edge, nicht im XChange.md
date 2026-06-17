# PDF wird im Edge statt PDF-XChange geöffnet

## Symptom

PDF-Dateien werden trotz korrekter Einstellungen im Microsoft Edge geöffnet und nicht im PDF-XChange Editor.

## Prüfung

- Standardprogramm kontrollieren
    
- PDF-Zuordnung prüfen
    
- Benutzeranmeldung prüfen
    

## Lösung

PowerShell oder Eingabeaufforderung als Administrator öffnen:

```text
gpupdate /force
```

Danach die Gruppenrichtlinien neu laden und erneut testen.

## Ergebnis

PDF-Dateien werden wieder korrekt im PDF-XChange Editor geöffnet.

## Hintergrund

Gruppenrichtlinien (Group Policies) können Programmzuordnungen und Systemeinstellungen steuern.

Wenn Richtlinien nicht aktuell sind, können falsche Zuordnungen verwendet werden.

Der Befehl `gpupdate /force` erzwingt das Neuladen der Richtlinien.

## Merksatz

Wenn Einstellungen korrekt aussehen, sich das System aber anders verhält, kann ein `gpupdate /force` helfen, die aktuellen Richtlinien neu anzuwenden.