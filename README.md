# Wissensbasis (HKB)

Eine leere Wissensbasis nach **HKF Core 1.0**. Dieses Verzeichnis ist zugleich
ein Obsidian-Vault und ein Git-Repository. Es enthält die Grundausstattung und
sonst nichts — keinen Inhalt, keine Bundles, kein Vokabular.

## Erste Schritte

1. **Verzeichnis in Obsidian als Vault öffnen.** Die Konfiguration unter
   `.obsidian/` ist bereits auf das Format eingestellt: Wikilinks statt
   Markdown-Links, vollständige Pfade, und die Property-Typen sind
   registriert, damit Obsidian Datum, Zahl und Liste richtig anzeigt.
2. **`name` in `hkb.md` ändern.** Dort steht der Anzeigename der
   Wissensbasis.
3. **Typen dazuladen oder eigene anlegen** — siehe unten.

## Was hier liegt

| Pfad | Inhalt |
|---|---|
| `hkb.md` | Wurzeldatei: Formatversion, Name, Pfade, Typtabelle |
| `AGENTS.md` | die Anleitung für Sprachmodelle und Werkzeuge |
| `CLAUDE.md` | verweist auf `AGENTS.md` |
| `typedefs/` | die 3 Basistypen `typedef`, `proptype`, `bundle` |
| `proptypes/` | die 12 Standard-Property-Typen |
| `bundles/` | je eine Notiz pro importiertem Bundle — noch leer |
| `media/` | `images`, `videos`, `audios`, `documents` — noch leer |

Diese 15 Notizen sind die **Grundausstattung**. Sie entsteht mit der
Wissensbasis und wird nicht geliefert; ohne sie ließe sich kein Bundle
beschreiben, das die Typen nachreicht.

## Core und Base

**HKF Core** beschreibt, wie eine Ablage aufgebaut ist — Verzeichnisse,
Wertformen, Verweise, Bundle-Format, Methoden. Es nennt keinen einzigen
inhaltlichen Typ, und genau das liegt hier: keine Person, kein Ort, keine
Quelle.

**HKF Base** ist das Vokabular dafür: neun Typdefinitionen für

    person · organisation · place · event · source · term · topic · note · specification

Es kommt als Bundle `hkf` und wird mit `hk-import` geladen. Danach steht in
`bundles/` eine Notiz, die festhält, was übernommen wurde, und jede
übernommene Notiz trägt die Zugehörigkeit in ihrer `bundles`-Property.

Der Import ist freiwillig. Wer andere Gegenstände verwaltet, legt einfach
eigene Typdefinitionen in `typedefs/` an. Ein Bundle ist nur nötig, wenn Typen
oder Inhalte weitergegeben werden sollen.

## Die Spezifikation

`hkf: "1.0"` in `hkb.md` sagt, welche Fassung von Core gilt. Wo sie zu lesen
ist, sagt die optionale Property `spec` — als URL oder als Verweis auf eine
eigene Notiz vom Typ `specification`. Die Wikilink-Form setzt allerdings
voraus, dass dieser Typ vorhanden ist, und er kommt erst mit Base. `spec` ist
hier nicht gesetzt; trag die Adresse ein, unter der du Core erreichst.

## Als Vorlage benutzen

Dieses Repository ist eine Vorlage. Auf GitHub erzeugt „Use this template"
daraus ein neues, eigenständiges Repository ohne Historie:

```
gh repo create meine-wissensbasis --template <benutzer>/<vorlage> --private
```
