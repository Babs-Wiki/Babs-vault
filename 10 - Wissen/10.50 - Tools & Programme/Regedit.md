# Regedit – Windows Registry Editor

**Regedit** ist das Windows-Werkzeug zum Anzeigen und Bearbeiten der Windows-Registrierung.

> **Merksatz:** Regedit ist das Werkzeug. Die Registry ist die zentrale Konfigurationsdatenbank von Windows.

---

<details>
<summary>📖 Was ist Regedit?</summary>

**Regedit** steht für **Registry Editor** beziehungsweise **Registrierungs-Editor**.

Mit diesem Windows-Werkzeug können Einträge in der Windows-Registry:

- angezeigt
- gesucht
- geprüft
- exportiert
- geändert
- neu erstellt
- gelöscht

werden.

Regedit zeigt die Registry in einer Baumstruktur an, ähnlich wie Ordner und Dateien im Windows-Explorer.

</details>

<details>
<summary>▶️ Regedit starten</summary>

### Über den Ausführen-Dialog

```text
Win + R
```

Danach eingeben:

```text
regedit
```

Anschliessend mit `Enter` bestätigen.

### Über die Windows-Suche

```text
Startmenü öffnen
        ↓
Regedit eingeben
        ↓
Registrierungs-Editor auswählen
```

Je nach Berechtigung erscheint eine Sicherheitsabfrage der Benutzerkontensteuerung.

</details>

<details>
<summary>🗄️ Was ist die Registry?</summary>

Die **Windows-Registry** ist eine zentrale Datenbank, in der Windows und viele Programme ihre Einstellungen speichern.

Sie enthält unter anderem:

- Windows-Einstellungen
- Benutzerprofile
- Hardware-Konfigurationen
- Programmeinstellungen
- Dateizuordnungen
- Sicherheitsrichtlinien
- Informationen über installierte Software
- Einstellungen für Dienste und Geräte

Man kann sich die Registry wie ein grosses, hierarchisch aufgebautes Verzeichnis für Systemeinstellungen vorstellen.

</details>

<details>
<summary>🧱 Aufbau der Registry</summary>

Die Registry besteht hauptsächlich aus:

- **Schlüsseln**
- **Unterschlüsseln**
- **Werten**
- **Wertdaten**

Beispiel:

```text
HKEY_LOCAL_MACHINE
└── SOFTWARE
    └── Microsoft
        └── Windows
```

Ein **Schlüssel** ähnelt einem Ordner.

Ein **Wert** enthält eine bestimmte Einstellung oder Information.

Beispiel:

```text
Schlüssel:
HKEY_LOCAL_MACHINE\SOFTWARE\Beispielprogramm

Wert:
Installationspfad

Wertdaten:
C:\Programme\Beispielprogramm
```

</details>

<details>
<summary>🗂️ Wichtige Hauptbereiche</summary>

### HKEY_LOCAL_MACHINE – HKLM

Enthält Einstellungen, die den gesamten Computer betreffen.

Beispiele:

- installierte Software
- Hardware
- Windows-Dienste
- systemweite Konfigurationen

### HKEY_CURRENT_USER – HKCU

Enthält Einstellungen des aktuell angemeldeten Benutzerkontos.

Beispiele:

- persönliche Programmeinstellungen
- Desktop-Einstellungen
- Benutzereinstellungen
- individuelle Dateizuordnungen

### HKEY_USERS – HKU

Enthält Registry-Bereiche der verschiedenen Benutzerprofile.

### HKEY_CLASSES_ROOT – HKCR

Enthält unter anderem:

- Dateizuordnungen
- Dateitypen
- Programmverknüpfungen
- Informationen darüber, welches Programm eine Datei öffnet

### HKEY_CURRENT_CONFIG – HKCC

Enthält Informationen zur aktuell verwendeten Hardwarekonfiguration.

</details>

<details>
<summary>🧾 Häufige Werttypen</summary>

Registry-Werte können unterschiedliche Datentypen besitzen.

| Werttyp | Bedeutung |
|---|---|
| `REG_SZ` | Einfacher Textwert |
| `REG_DWORD` | Ganze Zahl mit 32 Bit |
| `REG_QWORD` | Ganze Zahl mit 64 Bit |
| `REG_BINARY` | Binäre Daten |
| `REG_MULTI_SZ` | Mehrere Textwerte |
| `REG_EXPAND_SZ` | Textwert mit auflösbaren Umgebungsvariablen |

Der Werttyp muss zur erwarteten Einstellung passen.

Ein falscher Werttyp kann dazu führen, dass eine Einstellung nicht funktioniert.

</details>

<details>
<summary>💼 Typische Einsätze im Support</summary>

Regedit kann im Support oder bei der Fehleranalyse verwendet werden, um:

- Programmeinstellungen zu kontrollieren
- fehlerhafte Konfigurationen zu untersuchen
- Einträge nach einer Deinstallation zu prüfen
- Richtlinien und Systemeinstellungen zu kontrollieren
- Herstelleranleitungen umzusetzen
- Dateizuordnungen zu überprüfen
- bestimmte Benutzer- oder Computereinstellungen zu vergleichen

Regedit sollte jedoch nur verwendet werden, wenn bekannt ist:

- welcher Schlüssel betroffen ist
- welcher Wert erwartet wird
- welche Änderung vorgenommen werden soll
- wie der ursprüngliche Zustand wiederhergestellt werden kann

</details>

<details>
<summary>🔍 Einen Registry-Eintrag suchen</summary>

In Regedit kann über folgende Tastenkombination gesucht werden:

```text
Ctrl + F
```

Gesucht werden kann nach:

- Schlüsseln
- Wertnamen
- Wertdaten

Mit `F3` wird nach dem nächsten passenden Treffer gesucht.

Bei der Suche ist Vorsicht nötig, weil derselbe Begriff an mehreren Stellen vorkommen kann.

</details>

<details>
<summary>💾 Registry-Einträge sichern</summary>

Vor einer Änderung kann ein Schlüssel exportiert werden.

Vorgehen:

1. Den gewünschten Schlüssel markieren.
2. Rechtsklick auf den Schlüssel.
3. **Exportieren** auswählen.
4. Speicherort und Dateinamen festlegen.
5. Die Datei mit der Endung `.reg` speichern.

Dadurch wird eine Sicherung des ausgewählten Bereichs erstellt.

Eine exportierte `.reg`-Datei kann Registry-Einträge wieder eintragen. Sie sollte deshalb nur verwendet werden, wenn ihr Inhalt bekannt und vertrauenswürdig ist.

</details>

<details>
<summary>⚠️ Risiken und Sicherheitsregeln</summary>

Änderungen an der Registry können sofort wirksam werden.

Falsche Änderungen können:

- Programme beschädigen
- Windows-Funktionen beeinträchtigen
- Benutzerprofile beschädigen
- Sicherheitsprobleme verursachen
- Startprobleme auslösen
- dazu führen, dass Windows nicht mehr korrekt funktioniert

Darum gilt:

- nur bekannte und dokumentierte Änderungen durchführen
- den vollständigen Registry-Pfad kontrollieren
- Wertname, Werttyp und Wertdaten genau prüfen
- den betroffenen Schlüssel vorher exportieren
- keine fremden `.reg`-Dateien ungeprüft ausführen
- bei Unsicherheit keine Änderung vornehmen
- Änderungen nach Möglichkeit zuerst in einer Testumgebung prüfen

> **Wichtig:** Nicht jeder Registry-Eintrag kann durch das Zurücksetzen eines einzelnen Wertes vollständig repariert werden.

</details>

<details>
<summary>🧪 Vorgehen bei einer kontrollierten Prüfung</summary>

Bei einer Hersteller- oder Supportanleitung kann folgendes Vorgehen helfen:

1. Anleitung vollständig lesen.
2. Betroffenes System und Benutzerkonto prüfen.
3. Genauen Registry-Pfad kontrollieren.
4. Vorhandenen Wert dokumentieren.
5. Betroffenen Schlüssel exportieren.
6. Geforderte Änderung vornehmen.
7. Anwendung oder System neu starten, falls erforderlich.
8. Ergebnis testen.
9. Änderung und Testergebnis dokumentieren.
10. Bei Problemen den ursprünglichen Zustand wiederherstellen.

</details>

<details>
<summary>🔗 Siehe auch</summary>

- [Regedit im Glossar](<../10.10 - Glossar/R.md#regedit>)
- [Registry im Glossar](<../10.10 - Glossar/R.md#registry>)
- [Windows – Kurzbefehle & Befehle](<Windows – Kurzbefehle & Befehle.md>)

</details>