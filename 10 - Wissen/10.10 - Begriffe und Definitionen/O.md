-[OAuth](#oauth)

## OAuth

| Feld | Inhalt |
|------|--------|
| 🇬🇧 **Englisch** | Open Authorization |
| 🇩🇪 **Deutsch** | Offenes Verfahren zur Zugriffsfreigabe |
| 🎯 **Wozu dient das?** | OAuth ermöglicht einer Anwendung einen begrenzten Zugriff auf einen anderen Dienst, ohne dass sie das Passwort der Person erhalten muss. |
| 🧠 **Merksatz** | **OAuth gibt einer Anwendung einen begrenzten Schlüssel – aber nicht mein Passwort.** |

<details>
<summary>💡 Beispiel</summary>

Bei einer Anmeldung über Apple läuft es vereinfacht so:

1. Ich melde mich bei Apple an.
2. Apple bestätigt die erfolgreiche Anmeldung.
3. ChatGPT erhält einen digitalen Nachweis.
4. Mein Apple-Passwort wird nicht an ChatGPT weitergegeben.

Ähnlich funktioniert es, wenn eine Anwendung Zugriff auf bestimmte Daten eines anderen Dienstes erhalten soll.

</details>

<details>
<summary>📚 Mehr wissen</summary>

OAuth regelt hauptsächlich, **welcher Zugriff erlaubt wird**.

Es kann beispielsweise festgelegt werden:

- welche Anwendung Zugriff erhält,
- auf welche Daten sie zugreifen darf,
- wie lange der Zugriff gilt,
- ob die Erlaubnis wieder entzogen werden kann.

Für eine vollständige Anmeldung wird OAuth häufig mit einem zusätzlichen Verfahren zur Identitätsprüfung kombiniert.

</details>

<details>
<summary>⚙️ Technischer Hintergrund</summary>

Nach der Zustimmung erhält die Anwendung normalerweise ein **Access Token**.

Dieses Token kann eingeschränkte Rechte besitzen, beispielsweise:

- Daten nur lesen,
- bestimmte Daten bearbeiten,
- nur während einer begrenzten Zeit gültig sein.

Das Passwort bleibt beim ursprünglichen Anbieter und wird nicht an die andere Anwendung weitergegeben.

</details>

<details>
<summary>💼 Mein Arbeitsalltag</summary>

OAuth kann mir bei Webanwendungen, APIs und Schnittstellen begegnen.

Bei Tests kann wichtig sein, ob ein Token korrekt ausgestellt wird und ob nur die vorgesehenen Zugriffe erlaubt sind.

</details>

<details>
<summary>🔗 Siehe auch</summary>

- [API](A.md#api)
- [Authentifizierung](A.md#authentifizierung)
- [Token](T.md#token)

</details>