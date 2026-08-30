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
| `typedefs/` | die 3 Basistypen `typedef`, `proptype`, `bundle` |
| `proptypes/` | die 13 Standard-Property-Typen |
| `bundles/` | je eine Notiz pro importiertem Bundle — noch leer |
| `media/` | `images`, `videos`, `audios`, `documents` — noch leer |

Diese 16 Notizen sind die **Grundausstattung**. Sie entsteht mit der
Wissensbasis und wird nicht geliefert; ohne sie ließe sich kein Bundle
beschreiben, das die Typen nachreicht.

## Core und Base

[**HKF Core**](https://github.com/arpablo/hkf-spec/blob/main/HKF-Core-V1.0.md) beschreibt, wie eine Ablage aufgebaut ist —
Verzeichnisse, Wertformen, Verweise, Bundle-Format, Methoden. Es nennt keinen
einzigen inhaltlichen Typ, und genau das liegt hier: keine Person, kein Ort,
keine Quelle.

[**HKF Base**](https://github.com/arpablo/hkf-spec/blob/main/HKF-Base-V1.0.md) ist das Vokabular dafür: neun Typdefinitionen für

    person · organisation · place · event · source · term · topic · note · specification

Es kommt als Bundle [`hkf-base`](https://github.com/arpablo/hkf-base) und wird mit `hk-import` geladen.
Danach steht in `bundles/` eine Notiz, die festhält, was übernommen wurde, und
jede übernommene Notiz trägt die Zugehörigkeit in ihrer `bundles`-Property.

Der Import ist freiwillig. Wer andere Gegenstände verwaltet, legt einfach
eigene Typdefinitionen in `typedefs/` an. Ein Bundle ist nur nötig, wenn Typen
oder Inhalte weitergegeben werden sollen.

## Die Spezifikation

| Dokument | |
|---|---|
| [`HKF-Core-V1.0.md`](https://github.com/arpablo/hkf-spec/blob/main/HKF-Core-V1.0.md) | Wie eine Ablage aufgebaut ist |
| [`HKF-Base-V1.0.md`](https://github.com/arpablo/hkf-spec/blob/main/HKF-Base-V1.0.md) | Das Standardvokabular |

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
