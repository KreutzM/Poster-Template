# AGENTS.md

Hinweise für Codex CLI oder andere Coding-Agenten in diesem Poster-Repo.

## Ziel

Dieses Repository enthält eine neutrale, leere DIN-A0-LaTeX-Poster-Vorlage. Inhaltliche Änderungen sollen in `src/content/` erfolgen, zentrale Metadaten in `src/poster-config.tex`, Layout-Änderungen in `src/poster-theme.tex`.

## Build

```bash
make check
make preview
```

`make check` muss vor Abschluss erfolgreich sein. Danach `build/main.pdf` manuell prüfen.

## Regeln

- Keine generierten Dateien aus `build/` committen.
- Keine Logos oder Bilder ohne Rechteprüfung ergänzen.
- Keine numerischen Claims erfinden.
- Platzhalter dürfen in der leeren Vorlage existieren; vor finaler Abgabe `make final-check` nutzen.
- Sprache standardmäßig Deutsch, außer die Nutzer:innen wünschen Englisch.

## Typische Änderungsreihenfolge

1. `src/poster-config.tex` anpassen.
2. Einen Inhaltsblock in `src/content/` ersetzen.
3. Falls nötig Assets in `assets/` ergänzen.
4. `make check` ausführen.
5. PDF visuell prüfen.
