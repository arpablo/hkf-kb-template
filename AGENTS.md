# Meine Wissensbasis

Eine Wissensbasis im Format **HKF 1.0**. Einstieg ist `hkb.md`.
Zeiten gelten in `Europe/Berlin`.

## Sechs Regeln, bevor du etwas änderst

1. **Der Pfad bestimmt den Typ.** Eine Notiz gehört zu dem Typ, unter dessen
   Verzeichnis sie liegt; `type` im Frontmatter muss dazu passen.
2. **Erfinde keine Properties.** Was ein Typ zusichert, steht in
   `typedefs/<typ>.md`. Lies die Datei, bevor du ein Feld setzt.
3. **Verweise in Notizen sind qualifizierte Wikilinks mit Alias.** Das Ziel
   ist der vollständige Pfad ab der Vault-Wurzel ohne `.md`: das Verzeichnis,
   in dem diese Datei liegt, dann das Typverzeichnis, dann der Dateiname.
   Dahinter `|` und der Anzeigetext, in der Regel der `title` des Ziels. In
   einer Tabellenzelle wird der Strich als `\|` maskiert. Diese Datei und
   `hkb.md` verweisen dagegen relativ zu sich selbst, also ohne den ersten
   Abschnitt.
4. **Frontmatter bleibt flach.** Nur Text, Liste, Zahl, Checkbox, Datum,
   Datum mit Uhrzeit. Keine verschachtelten Abbildungen, keine leeren Werte.
5. **Wenn du änderst, schreib es hin.** `modified` auf jetzt, `modified_by`
   auf deinen Modellnamen.
6. **`typedefs/` und `proptypes/` sind tabu.** Sie gehören zur
   Grundausstattung oder kommen aus einem Bundle. Eigene Typen legst du
   daneben.

## Typen dieser Wissensbasis

| Typ | Verzeichnis | Zweck |
|---|---|---|
| bundle | bundles | Beschreibt eine Lieferung. |
| proptype | proptypes | Schränkt eine Wertform ein. |
| typedef | typedefs | Registriert einen Typ und legt sein Verzeichnis fest. |

Mediendateien liegen unter `media/` in `images`, `videos`, `audios` oder
`documents` — Verweise darauf behalten die Dateiendung.

## Hinweise

<!-- Dieser Abschnitt bleibt bei einer Neuerzeugung erhalten. -->

Noch keine.
