# Wissensbasis (HKB)

Eine leere Wissensbasis nach dem **Henni Knowledge Format, Fassung 1.0**.
Dieses Verzeichnis ist zugleich ein Obsidian-Vault und ein Git-Repository.
Es enthält die Grundausstattung und sonst nichts — keinen Inhalt, keine
Bundles.

## Erste Schritte

1. **Verzeichnis in Obsidian als Vault öffnen.** Die Konfiguration unter
   `.obsidian/` ist bereits auf das Format eingestellt: Wikilinks statt
   Markdown-Links, vollständige Pfade, und die Property-Typen sind
   registriert, damit Obsidian Datum, Zahl und Liste richtig anzeigt.
2. **`name` in `hkb.md` ändern.** Dort steht der Anzeigename der
   Wissensbasis.
3. **Notizen anlegen.** Jede Notiz liegt im Verzeichnis ihres Typs. Welche
   Typen es gibt, steht in der Tabelle `# Typen` in `hkb.md`.

## Was hier liegt

| Pfad | Inhalt |
|---|---|
| `hkb.md` | Wurzeldatei: Formatversion, Name, Pfade, Typtabelle |
| `AGENTS.md` | die Anleitung für Sprachmodelle und Werkzeuge |
| `CLAUDE.md` | verweist auf `AGENTS.md` |
| `typedefs/` | die drei Basistypen `typedef`, `proptype`, `bundle` |
| `proptypes/` | die zwölf Standard-Property-Typen |
| `bundles/` | je eine Notiz pro importiertem Bundle — noch leer |
| `media/` | `images`, `videos`, `audios`, `documents` — noch leer |

Diese fünfzehn Notizen sind die **Grundausstattung**. Sie entsteht mit der
Wissensbasis und wird nicht geliefert; ohne sie liesse sich kein Bundle
beschreiben, das die Typen nachreicht.

## Typen dazuladen

Die Grundausstattung kennt keinen einzigen inhaltlichen Typ — keine Person,
keinen Ort, keine Quelle. Die kommen aus dem Bundle **`hkf`**, das die neun
Standardtypen liefert:

    person · organisation · place · event · source · term · topic · note · specification

Importiert wird es mit der Methode `hk-import`. Danach steht in `bundles/`
eine Notiz, die festhält, was übernommen wurde, und jede übernommene Notiz
trägt die Zugehörigkeit in ihrer `bundles`-Property.

Wer eigene Typen braucht, legt einfach eine Notiz in `typedefs/` an. Ein
Bundle ist nur nötig, wenn Typen oder Inhalte weitergegeben werden sollen.

## Die Spezifikation

`hkf: "1.0"` in `hkb.md` sagt, welche Fassung des Formats gilt. Wo sie zu
lesen ist, sagt die optionale Property `spec` — entweder als URL oder als
Verweis auf eine eigene Notiz vom Typ `specification`. Sie ist hier nicht
gesetzt; trag die Adresse ein, unter der du die Spezifikation erreichst.

## Als Vorlage benutzen

Dieses Repository ist eine Vorlage. Auf GitHub erzeugt „Use this template"
daraus ein neues, eigenständiges Repository ohne Historie:

```
gh repo create meine-wissensbasis --template <benutzer>/<vorlage> --private
```
