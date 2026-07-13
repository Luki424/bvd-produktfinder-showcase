# BVD Produktfinder – Arbeitsnotizen für Claude Code

## Arbeitsweise (Modell-Split, tokensparend)
- **Fable 5** macht die **Vorarbeit** (Recherche, Audits, Analyse) und liefert eine
  präzise, ausführungsfertige Vorlage.
- **Opus 4.8** übernimmt die **Ausführung** (exakte Edits, Verifikation, Deploy).
- Ziel: Tokens sparen. Zwischen den Modellen selbständig wechseln – Vorarbeit an
  einen Fable-5-Subagenten delegieren (`Agent`-Tool mit `model: "fable"`), Ergebnis
  dann mit Opus umsetzen.

## Projekt
- Single-File-App: `index.html` (React + Vite, minifiziert, ~585 KB). CSS steckt in
  einem `<style rel="stylesheet" crossorigin>…</style>`-Block. Bearbeitung über
  kleine Node-Skripte mit exaktem Anker-String (`split(anchor)`, genau 1 Treffer).
- PWA: `sw.js` (network-first Navigation, stale-while-revalidate Assets),
  `site.webmanifest`. i18n-Laufzeitschicht (DE/EN) + Hell-/Dunkelmodus.
- Hosting: GitHub Pages, `https://luki424.github.io/bvd-produktfinder-showcase/`.

## Feste Vorgaben
- **Keine Preise** öffentlich.
- **Produktdaten bleiben in Originalsprache** (Technologie/Kategorie/Marke/
  Anwendungen nicht als Daten übersetzen; nur beschreibende UI-Labels).
- **Nie Daten erfinden** (z. B. Öffnungszeiten nur nach Bestätigung).
- Jede Änderung: mit Playwright verifizieren → committen → PR → Rebase-Merge →
  Branch von `main` zurücksetzen.

## Verifikation (Sandbox)
- Playwright über `scratchpad/serve.js`; Chromium unter
  `/opt/pw-browsers/chromium-1194/chrome-linux/chrome`; `NODE_PATH=/opt/node22/lib/node_modules`.
- Externe Produktbilder (bvd-batterien.de) sind in der Sandbox nicht erreichbar
  (ERR_TUNNEL) – kein App-Fehler.
