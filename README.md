# Spillway Carwash & Grill — Source Code

This ZIP contains the complete static website, all 88 menu items, item photographs, fonts and image credits from the latest deployed version (version 3).

## Run on your computer

1. Extract this ZIP.
2. Open a terminal or Command Prompt inside the extracted `spillway-menu-source` folder.
3. Start a local server using the command for your system below.
4. Open http://127.0.0.1:8000 in your browser.

### Windows (Python installed)

```bat
py -m http.server 8000 --bind 127.0.0.1 --directory dist
```

### macOS / Linux (Python 3 installed)

```sh
python3 -m http.server 8000 --bind 127.0.0.1 --directory dist
```

Press Ctrl+C in the terminal to stop the server. Use a local HTTP server to load the JSON menu files; opening `index.html` directly as a file will not load them reliably.

## Project files

| File | Purpose |
| --- | --- |
| `dist/index.html` | Page structure and sections |
| `dist/styles.css` | Colours, typography, layouts and mobile styles |
| `dist/app.js` | Menu browsing, search, saved items, platter finder and table list |
| `dist/menu.json` | Menu names, categories, descriptions, serving formats and prices |
| `dist/menu-photos.json` | Item photo mapping and source credits |
| `dist/assets/` | All local images, logo, fonts and font licence |
| `IMAGE-SOURCES.md` | Links and credits for sourced photographs |
| `SOURCE-NOTES.md` | Original project notes and previous validation details |
| `VERSION.json` | Exported version and source commit |

The website uses plain HTML, CSS and JavaScript. There is no build step, database or package installation.

## Make changes

- Change menu items and prices in `dist/menu.json`. Keep item IDs stable to preserve saved favourites and table lists.
- Update image paths and credits in `dist/menu-photos.json`.
- Change the design in `dist/styles.css` and page wording in `dist/index.html`.
- Change interactions in `dist/app.js`.

Saved favourites and table lists use the visitor's browser storage. The table list is shown to a server to place an order; it does not send online orders or take payments.

## Hosting and access

The deployed website's private sign-in is supplied by its hosting service. This source archive contains the static frontend, without that hosting sign-in service. Local serving with the commands above is bound to your own computer. A separate host needs its own access controls if you want it private.

Image credits and applicable licences are included with the source. Retain these when reusing the assets.
