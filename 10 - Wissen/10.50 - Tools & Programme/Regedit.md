# Regedit

## Definition

Regedit (Registry Editor) ist das Windows-Werkzeug zum Anzeigen und Bearbeiten der Windows-Registrierung (Registry).

Die Registry ist eine zentrale Datenbank, in der Windows sowie viele Programme ihre Einstellungen speichern.

---

## Starten

### Über Ausführen

Win + R

regedit

### Über die Suche

Startmenü → Regedit eingeben

---

## Was ist die Registry?

Die Registry enthält unter anderem:

- Windows-Einstellungen
- Benutzerprofile
- Hardware-Konfigurationen
- Programm-Einstellungen
- Sicherheitseinstellungen

Man kann sich die Registry wie ein riesiges Verzeichnis oder Telefonbuch von Windows vorstellen.

---

## Aufbau

Die Registry besteht aus sogenannten Schlüsseln (Keys) und Werten (Values).

Beispiel:

HKEY_LOCAL_MACHINE
└── Software
    └── Microsoft

Wichtige Hauptbereiche:

- HKEY_LOCAL_MACHINE (HKLM)
  → Einstellungen für den gesamten Computer

- HKEY_CURRENT_USER (HKCU)
  → Einstellungen des aktuell angemeldeten Benutzers

- HKEY_USERS
  → Benutzerprofile

- HKEY_CLASSES_ROOT
  → Dateizuordnungen und Programmverknüpfungen

---

## Typische Einsätze im Support

- Programmeinstellungen prüfen
- Fehler analysieren
- Einträge nach Deinstallationen kontrollieren
- Richtlinien und Konfigurationen überprüfen
- Herstelleranleitungen umsetzen

---

## Achtung

Änderungen an der Registry wirken oft sofort.

Falsche Änderungen können:

- Programme beschädigen
- Windows-Funktionen beeinträchtigen
- Startprobleme verursachen

Deshalb vor Änderungen immer sorgfältig prüfen.

---

## Merksatz

Regedit ist das Werkzeug zum Anzeigen und Bearbeiten der Windows-Registry.
Die Registry ist die zentrale Konfigurationsdatenbank von Windows.