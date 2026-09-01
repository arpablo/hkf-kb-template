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
| `Typedefs/` | die 20 Basistypen `typedef`, `proptype`, `bundle` |
| `Proptypes/` | die 16 Standard-Property-Typen |
| `Bundles/` | je eine Notiz pro importiertem Bundle — noch leer |
| `Media/` | `Images`, `Videos`, `Audios`, `Documents` — noch leer |

Diese 36 Notizen sind die **Grundausstattung**. Sie entsteht mit der
Wissensbasis und wird nicht geliefert; ohne sie ließe sich kein Bundle
beschreiben, das die Typen nachreicht.

## Core und Config

[**HKF Core**](https://github.com/arpablo/hkf-spec/blob/main/HKF-Core-V1.0.md) beschreibt, wie eine Ablage aufgebaut ist —
Verzeichnisse, Wertformen, Verweise, Bundle-Format, Methoden. Es nennt keinen
einzigen inhaltlichen Typ, und genau das liegt hier: keine Person, kein Ort,
keine Quelle.

[**HKF Config**](https://github.com/arpablo/hkf-spec/blob/main/HKF-Config-V1.0.md) nennt daneben jede Typdefinition und jeden
Property-Typ. Drei Typen und vierzehn Property-Typen davon liegen hier als
Grundausstattung; die übrigen vierzehn sind das Vokabular:

    person · organisation · place · city · country · event · source
    term · concept · comparison · topic · note · specification · hint

Alle zwanzig liegen hier. Geliefert wird davon nichts — was jede Wissensbasis
ohnehin bekommt, muss niemand ausliefern. Ein Bundle bringt Inhalte mit und,
wenn es einen Typ braucht, den Config nicht kennt, dessen Typdefinition dazu;
geladen wird es mit [`hk-import`](https://github.com/arpablo/hkf-harness). Danach steht in `Bundles/`
eine Notiz, die festhält, was übernommen wurde.

Wer andere Gegenstände verwaltet, legt eigene Typdefinitionen in `Typedefs/`
an und lässt die ungenutzten liegen.

## Die Spezifikation

| Dokument | |
|---|---|
| [`HKF-Core-V1.0.md`](https://github.com/arpablo/hkf-spec/blob/main/HKF-Core-V1.0.md) | Wie eine Ablage aufgebaut ist |
| [`HKF-Config-V1.0.md`](https://github.com/arpablo/hkf-spec/blob/main/HKF-Config-V1.0.md) | Alle Typdefinitionen und Property-Typen |

Beide liegen im Repository [`hkf-spec`](https://github.com/arpablo/hkf-spec).

`hkf: "1.0"` in `hkb.md` sagt, welche Fassung von Core gilt, `spec`, wo sie zu
lesen ist — hier die öffentliche Adresse des Dokuments.

Statt einer URL darf dort auch ein Verweis auf eine eigene Notiz vom Typ
`specification` stehen, die das Dokument beschreibt oder enthält. Das setzt
allerdings voraus, dass dieser Typ vorhanden ist, und er kommt erst mit Base.

## Als Vorlage benutzen

Dieses Repository ist eine Vorlage. Auf GitHub erzeugt „Use this template"
daraus ein neues, eigenständiges Repository ohne Historie:

```
gh repo create meine-wissensbasis --template arpablo/hkf-kb-template --private
```
