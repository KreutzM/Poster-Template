# Bild-Assets und Image-Modelle

Dieses Dokument beschreibt, wie neue Poster-Abbildungen sicher und reproduzierbar vorbereitet werden koennen.

## Geeignete Einsatzfaelle fuer generierte Bilder

Generierte Bilder eignen sich gut fuer:

- Konzeptillustrationen,
- Prozessgrafiken,
- einfache Icons,
- visuelle Metaphern,
- Platzhalter fuer spaetere finale Grafiken,
- nicht-datengetriebene Hintergrund- oder Erklaerbilder.

Nicht geeignet sind generierte Bilder als Ersatz fuer:

- echte Messergebnisse,
- wissenschaftliche Datenplots,
- Screenshots von Software, die exakt stimmen muessen,
- Logos oder geschuetzte Marken ohne Rechteklaerung,
- Abbildungen, die eine reale Person, ein reales Produkt oder eine reale Messung exakt wiedergeben sollen.

## Empfohlene Bildanforderungen

Fuer DIN-A0-Poster sollten Abbildungen:

- kontrastreich sein,
- wenige Details enthalten,
- auch aus 1--2 m Abstand verstaendlich bleiben,
- moeglichst wenig eingebetteten Text enthalten,
- einen ruhigen Hintergrund haben,
- als PNG, PDF oder SVG-zu-PDF eingebunden werden,
- in finaler Druckgroesse ausreichend aufgeloest sein.

Fuer Rastergrafiken sind 150--300 dpi in finaler Druckgroesse ein sinnvoller Zielbereich. Fuer Diagramme und schematische Darstellungen sind Vektorformate vorzuziehen.

## Beispielauftrag fuer ein Image-Model

```text
Erzeuge eine klare, wissenschaftlich wirkende Flat-Illustration fuer ein DIN-A0-Poster.
Thema: ...
Motiv: ...
Stil: minimal, modern, hoher Kontrast, helle Flaechen, keine kleinen Details.
Wichtig: ohne Text, ohne Logos, ohne erfundene Zahlen, ohne realistische Personen.
Format: breit, geeignet als zentrale Posterabbildung.
```

## Ablage im Repo

Empfohlene Pfade:

- `assets/figures/main-figure.png` fuer die Hauptabbildung,
- `assets/figures/process-diagram.pdf` fuer Prozessgrafiken,
- `assets/logos/` nur fuer freigegebene Logos,
- `assets/qr/qr-code.png` fuer den QR-Code.

Jedes externe oder generierte Asset sollte in `docs/asset-inventory.md` dokumentiert werden.

## Einbindung in LaTeX

Die Vorlage nutzt im Standardblock `src/content/05_figure.tex` die zentrale Hauptabbildung. Passe dort Pfad und Bildunterschrift an.

Beispiel:

```tex
\PosterGraphic{assets/figures/main-figure.png}{Kurze, aussagekraeftige Bildunterschrift.}{Hauptabbildung}
```

## Pruefung vor Abgabe

Vor Druck oder Veroeffentlichung pruefen:

- Ist die Abbildung aus der Distanz lesbar?
- Ist sie fachlich korrekt und nicht irrefuehrend?
- Sind Rechte, Lizenz und Quelle dokumentiert?
- Gibt es keine eingebetteten Tippfehler oder unlesbaren Kleinsttext?
- Passt die Bildunterschrift zur tatsaechlichen Aussage der Abbildung?
