# Codex-Workflow fuer DIN-A0-Poster

Diese Vorlage ist so aufgebaut, dass Codex CLI ein Poster schnell textlich, strukturell und visuell iterieren kann.

## Grundprinzip

Codex soll nicht nur LaTeX-Code bearbeiten, sondern nach groesseren Schritten das gerenderte Poster pruefen.

Empfohlene Reihenfolge:

1. Inhalt und Metadaten anpassen.
2. `make check` ausfuehren.
3. `make preview` ausfuehren.
4. Die erzeugte Datei `build/poster-preview.png` visuell pruefen.
5. Layout, Textdichte und Abbildungsgoesse iterativ verbessern.

Die PNG-Vorschau ist der wichtigste Artefakt fuer visuelle Bewertung, weil Layout, Lesbarkeit und Abstaende daran besser beurteilt werden koennen als am LaTeX-Code allein.

## Neues Poster aus einem Thema erstellen

Beispielauftrag an Codex:

```text
Erstelle aus dieser Vorlage ein DIN-A0-Poster zum Thema "...".
Zielgruppe: ...
Event: ...
Kernaussage: ...

Arbeite in dieser Reihenfolge:
1. Passe src/poster-config.tex an.
2. Ersetze die Inhalte in src/content/*.tex.
3. Nutze kurze, postergeeignete Texte.
4. Verwende eine grosse zentrale Abbildung oder einen Platzhalter.
5. Fuehre make check aus.
6. Fuehre make preview aus.
7. Bewerte build/poster-preview.png visuell und optimiere Layout und Textdichte.
```

## Poster aus Abstract, Paper oder Notizen erstellen

Beispielauftrag:

```text
Erstelle ein verstaendliches DIN-A0-Konferenzposter aus den folgenden Notizen oder dem folgenden Abstract.
Erfinde keine Zahlen, Quellen oder Ergebnisse.
Markiere unklare Claims als TODO.
Reduziere Text stark und priorisiere eine klare Storyline.
```

## Visuelle Iteration

Nach dem Rendern sollte die PNG-Vorschau mit Bild-Input geprueft werden. Geeignete Pruefkriterien:

- Titel und Kernaussage sind aus Distanz schnell erfassbar.
- Die Leserichtung ist eindeutig.
- Die drei Spalten sind optisch ausgewogen.
- Keine Box wirkt ueberfuellt.
- Abbildungen sind gross genug und nicht textlastig.
- QR-Code, Kontakt und Event sind gut auffindbar.
- Die Aussenraender sind drucksicher.

## Empfohlene Iterationsschleife

1. Inhalt grob einsetzen.
2. `make check` ausfuehren.
3. `make preview` ausfuehren.
4. PNG visuell pruefen.
5. Text kuerzen und Layout anpassen.
6. Wiederholen, bis das Poster auf einer Gesamtseitenansicht ausgewogen wirkt.
7. Fachliche Endpruefung durch einen Menschen.

## Grenzen

- Codex kann Layout und Lesbarkeit unterstuetzen, ersetzt aber keine fachliche Pruefung.
- Codex soll keine Messwerte oder Ergebnisse erfinden.
- Generierte Bilder sind fuer Konzeptgrafiken geeignet, nicht als Ersatz fuer echte wissenschaftliche Datenplots.
- Vor Veroeffentlichung muessen Bildrechte, Logo-Nutzung und QR-Code-Ziel geprueft werden.
