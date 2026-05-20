# LaTeX DIN-A0 Poster Template

Leere, gut dokumentierte Vorlage für wissenschaftliche DIN-A0-Poster im Hochformat. Die Vorlage basiert strukturell auf einem Overleaf-/beamerposter-Poster, ist aber neutralisiert und so aufgebaut, dass sie lokal, in Overleaf oder in Git-Repos reproduzierbar gepflegt werden kann.

## Schnellstart

```bash
make pdf
```

Das PDF liegt danach unter:

```text
build/main.pdf
```

Für eine PNG-Vorschau:

```bash
make preview
```

## Struktur

| Pfad | Zweck |
|---|---|
| `main.tex` | Root-Datei und Poster-Raster |
| `src/preamble.tex` | LaTeX-Pakete, A0-Format, Caption-Setup |
| `src/poster-config.tex` | Titel, Autor:innen, Logos, Farben, Kontakt, Abstände |
| `src/poster-theme.tex` | Boxen, Makros, Platzhalter, typografisches Design |
| `src/content/` | Inhaltliche Posterblöcke |
| `assets/logos/` | optionale Logos |
| `assets/figures/` | optionale Abbildungen |
| `assets/qr/` | optionaler QR-Code |
| `docs/` | Layout-, Inhalts- und Druckhinweise |
| `scripts/` | einfache Qualitätschecks |

## Editier-Reihenfolge

1. `src/poster-config.tex`: Titel, Autor:innen, Event, Kontakt, Farben und Logos anpassen.
2. `src/content/*.tex`: Inhalte blockweise ersetzen.
3. `assets/`: Logos, Abbildungen und QR-Code ergänzen.
4. `src/poster-theme.tex`: Nur bei Bedarf Layout, Boxen und Abstände ändern.
5. `make check` ausführen und PDF manuell prüfen.

## Empfohlenes Poster-Prinzip

Ein A0-Poster wird meist aus 1–2 m Entfernung gelesen. Deshalb sollte es eine klare visuelle Hierarchie haben:

- eine zentrale Botschaft direkt unter dem Titel,
- kurze Blöcke statt langer Fließtexte,
- wenige, große Abbildungen statt vieler kleiner Screenshots,
- messbare Kernaussagen als große Kennzahlen,
- QR-Code und Kontakt unten oder seitlich,
- sichere Außenränder für den Druck.

## Platzhalter und finale Prüfung

Die Vorlage baut auch ohne externe Bilder. Fehlende Logos und Abbildungen werden als Platzhalter gerendert. Vor der Abgabe kannst du prüfen, ob noch Platzhaltertexte enthalten sind:

```bash
make final-check
```

`make final-check` ist bewusst strenger als `make check`.

## Voraussetzungen

Unter Debian/Ubuntu sind diese Pakete typischerweise ausreichend:

```bash
sudo apt-get update
sudo apt-get install latexmk texlive-latex-extra texlive-lang-german texlive-fonts-recommended lmodern python3 poppler-utils
```

`poppler-utils` wird nur für `make preview` benötigt.
