# Layout-Guide für DIN-A0-Poster

## Was gegenüber einer einfachen Overleaf-Vorlage verbessert wurde

- Zentrale Konfiguration für Titel, Kontakt, Farben, Logos und Abstände in `src/poster-config.tex`.
- Inhalt, Design und Build-Logik sind getrennt.
- Drei gleich breite Spalten reduzieren Zeilenlängen und verbessern die Lesbarkeit.
- Eine vollbreite Take-away-Zeile zwingt zu einer klaren Kernbotschaft.
- Logos und Abbildungen sind optional: Die Vorlage kompiliert auch ohne Assets.
- Kennzahlen, Tags, Abbildungsplatzhalter und Kontaktblock sind als Makros wiederverwendbar.
- Standardisierte Build-, Preview- und Final-Checks erleichtern die Arbeit in Git, Overleaf und CI.

## Format

- DIN A0 Hochformat: ca. 841 × 1189 mm.
- Sichere Außenränder: mindestens 15–20 mm, besser 20–25 mm.
- Für Druckdaten beim Anbieter prüfen: Beschnittzugabe, Farbprofil, Mindestauflösung und PDF/X-Anforderungen.

## Typografie

- Titel: sehr groß, maximal zwei Zeilen.
- Blocktitel: kurz und eindeutig.
- Fließtext: kurze Absätze; lieber Listen und Abbildungen.
- Vermeide Blocksatz bei sehr schmalen Spalten, wenn unschöne Wortabstände entstehen. Die Vorlage nutzt `\justifying`, kann aber blockweise auf `\raggedright` geändert werden.

## Abbildungen

- Lieber eine große Hauptabbildung als viele kleine Einzelbilder.
- Rastergrafiken: 150–300 dpi in finaler Druckgröße.
- Vektorgrafiken bevorzugt als PDF/SVG-konvertiertes PDF.
- Bildunterschriften erklären Bedeutung, nicht nur Inhalt.

## QR-Code

- QR-Code groß genug drucken, typischerweise mindestens 25–30 mm Kantenlänge.
- Vor dem Druck mit mehreren Smartphones testen.
- Zusätzlich kurze URL als Text angeben, falls der QR-Code nicht scannt.
