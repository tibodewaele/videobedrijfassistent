# Videobedrijfassistent — Contour landing site

Statische landing-page voor Contour (videobedrijf-assistent project).

## Lokaal bekijken

Open `index.html` in een browser. Geen build-stap nodig.

```sh
open index.html
```

## Repo-structuur

```
.
├── index.html                  # Live website (alle assets ingebed als base64)
├── src/
│   └── contour-landing.html    # Bron-HTML zonder ingebedde assets (voor edits)
├── project-assets/
│   ├── images/                 # Foto's gebruikt in/voor de site
│   ├── videos-web/             # Web-geschikte video's (< 100MB)
│   ├── videos-4k/              # 4K master-files (lokaal, NIET in git — zie .gitignore)
│   └── docs/                   # Pitch, briefing, prijsoverzicht, marktonderzoek
└── skills/
    └── pdf-section-layout.skill
```

## Belangrijk: twee HTML-versies

- **`index.html`** — werkende website. Alle video's en logo's zitten als base64 in het bestand. ~70MB, traag om te laden, maar zelfstandig.
- **`src/contour-landing.html`** — clean broncode (~87KB), verwijst naar losse asset-bestanden (`HEATHER_hero.mp4`, `logo-bdsv.png`, …). Werkt **niet** zoals hij is, want die losse assets staan momenteel niet in de repo — ze zitten enkel base64-gecodeerd in `index.html`.

Wil je verder werken aan de site, dan is de volgende stap de assets uit `index.html` te extraheren naar losse files zodat `src/contour-landing.html` als echte broncode bruikbaar wordt.

## 4K-video's

De master-files in `project-assets/videos-4k/` (~1GB) zijn te groot voor GitHub en worden via `.gitignore` uitgesloten. Ze blijven lokaal in Google Drive bewaard.
