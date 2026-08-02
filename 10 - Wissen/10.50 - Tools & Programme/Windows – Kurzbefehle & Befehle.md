

Diese Seite enthält häufig verwendete Elemente der Windows-Benutzeroberfläche, Tastenkombinationen und nützliche Befehle.

> **Merksatz:** Tastenkombinationen und Befehle helfen dabei, Windows schneller zu bedienen und Probleme gezielt zu untersuchen.

---

<details>
<summary>🪟 Windows-Benutzeroberfläche</summary>

| Begriff | Bedeutung |
|---|---|
| **Windows-Suche** | Suchfunktion von Windows zum Finden von Programmen, Dateien und Einstellungen |
| **Ausführen-Dialog** | Eingabefenster zum direkten Starten von Programmen und Befehlen |
| **Explorer** | Programm zum Anzeigen und Verwalten von Dateien und Ordnern |
| **Taskleiste** | Leiste am unteren Bildschirmrand mit geöffneten und angehefteten Programmen |
| **Startmenü** | Menü der Windows-Taste mit Programmen, Suche und Systemeinstellungen |

### Windows-Suche öffnen

Die Windows-Suche kann über die **Windows-Taste** geöffnet werden.

Danach kann direkt ein Begriff eingegeben werden, beispielsweise:

- Ereignisanzeige
- Einstellungen
- Drucker
- Geräte-Manager
- Systeminformationen

### Ausführen-Dialog öffnen

```text
Win + R
```

Im Ausführen-Dialog können Programme und Befehle direkt gestartet werden.

Beispiele:

| Eingabe | Funktion |
|---|---|
| `winver` | Installierte Windows-Version anzeigen |
| `cmd` | Eingabeaufforderung öffnen |
| `regedit` | Registrierungs-Editor öffnen |
| `eventvwr` | Ereignisanzeige öffnen |

</details>

<details>
<summary>⌨️ Allgemeine Tastenkombinationen</summary>

| Tastenkombination | Funktion |
|---|---|
| `Ctrl + C` | Kopieren |
| `Ctrl + V` | Einfügen |
| `Ctrl + X` | Ausschneiden |
| `Ctrl + Z` | Letzte Aktion rückgängig machen |
| `Ctrl + Y` | Rückgängig gemachte Aktion wiederholen |
| `Ctrl + A` | Alles markieren |
| `Ctrl + F` | Suchen |
| `Ctrl + S` | Speichern |
| `Ctrl + P` | Drucken oder – abhängig vom Programm – eine Befehlsauswahl öffnen |
| `Alt + F4` | Aktives Fenster schliessen |

> **Hinweis:** Die Funktion einer Tastenkombination kann je nach verwendetem Programm leicht abweichen.

</details>

<details>
<summary>🖥️ Windows-Tastenkombinationen</summary>

| Tastenkombination | Funktion |
|---|---|
| `Win + R` | Ausführen-Dialog öffnen |
| `Win + E` | Windows-Explorer öffnen |
| `Win + L` | Computer sperren |
| `Win + D` | Desktop anzeigen oder wieder ausblenden |
| `Win + I` | Windows-Einstellungen öffnen |
| `Win + V` | Zwischenablageverlauf öffnen |
| `Win + Shift + S` | Bildschirmausschnitt erstellen |
| `Alt + Tab` | Zwischen geöffneten Fenstern wechseln |
| `Ctrl + Shift + Esc` | Task-Manager öffnen |
| `Shift + Herunterfahren` | Windows vollständig herunterfahren und den Schnellstart umgehen |

### Vollständiges Herunterfahren mit Shift

1. Das Startmenü öffnen.
2. Auf **Ein/Aus** klicken.
3. Die `Shift`-Taste gedrückt halten.
4. Auf **Herunterfahren** klicken.

Dadurch wird Windows vollständig heruntergefahren, anstatt den Zustand teilweise für den Schnellstart zu speichern.

</details>

<details>
<summary>🛠️ Nützliche Windows-Befehle</summary>

| Befehl | Funktion |
|---|---|
| `winver` | Installierte Windows-Version und Build-Nummer anzeigen |
| `gpupdate /force` | Gruppenrichtlinien sofort neu laden |
| `shutdown /p` | Computer sofort und vollständig herunterfahren |
| `shutdown /r /t 0` | Computer sofort neu starten |
| `ipconfig` | Netzwerkkonfiguration anzeigen |
| `hostname` | Namen des Computers anzeigen |
| `whoami` | Aktuell angemeldetes Benutzerkonto anzeigen |

### `winver`

Mit diesem Befehl wird angezeigt:

- installierte Windows-Version
- Versionsnummer
- Betriebssystem-Build

Der Befehl kann über `Win + R` eingegeben werden.

### `gpupdate /force`

Dieser Befehl fordert Windows auf, die Gruppenrichtlinien sofort neu zu laden.

Das kann beispielsweise helfen, wenn zentrale Einstellungen geändert wurden, aber auf dem Computer noch nicht wirksam sind.

Der Befehl wird normalerweise in der Eingabeaufforderung oder PowerShell ausgeführt:

```text
gpupdate /force
```

Nach der Aktualisierung kann eine Abmeldung oder ein Neustart erforderlich sein.

### `shutdown /p`

Dieser Befehl fährt den Computer sofort und vollständig herunter:

```text
shutdown /p
```

> **Achtung:** Programme werden dabei unmittelbar geschlossen. Nicht gespeicherte Arbeit kann verloren gehen.

### Sofortiger Neustart

```text
shutdown /r /t 0
```

Bedeutung:

- `/r` = Neustart
- `/t 0` = keine Wartezeit

</details>

<details>
<summary>💡 Beispiele aus meinem Arbeitsalltag</summary>

### Windows-Version kontrollieren

```text
Win + R
↓
winver eingeben
↓
Enter drücken
```

Damit kann geprüft werden, welche Windows-Version und welcher Build installiert sind.

### Gruppenrichtlinien aktualisieren

Wenn eine zentrale Einstellung noch nicht übernommen wurde:

```text
Eingabeaufforderung oder PowerShell öffnen
↓
gpupdate /force eingeben
↓
Aktualisierung abwarten
↓
Anwendung erneut testen
```

### Explorer öffnen

```text
Win + E
```

Damit kann schnell auf Dateien, Ordner und Netzlaufwerke zugegriffen werden.

### Zwischen Anwendungen wechseln

```text
Alt + Tab
```

Damit kann beispielsweise schnell zwischen einer Fachanwendung, Excel, GitHub und einem Ticketsystem gewechselt werden.

</details>

<details>
<summary>⚠️ Hinweise</summary>

- Befehle sollten nur ausgeführt werden, wenn ihre Wirkung bekannt ist.
- Vor einem Herunterfahren oder Neustart müssen offene Arbeiten gespeichert werden.
- Manche Befehle benötigen Administratorrechte.
- Gruppenrichtlinien werden zentral verwaltet und können lokale Einstellungen überschreiben.
- `regedit` verändert die Windows-Registrierung und sollte nur mit besonderer Vorsicht verwendet werden.

</details>