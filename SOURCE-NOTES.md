# Spillway Carwash & Grill menu

Private static menu website. Hosting access must remain owner-private until the owner explicitly approves a broader audience.

## Content

`dist/menu.json` contains 88 menu items, sourced from the user's **SPILLWAY BAR 2026 PRICING REVISED 6 JUNE .xlsx**, with unpriced sides completed from **Spillway menu (1).pdf** and **Spillway_Menu_Updated.pdf**. The corrected Windhoek Lager bottle price is K45. Spreadsheet prices take precedence over the older artwork, including Savanna at K50. Standard brand spelling is used where source labels contain obvious spelling errors. Platter contents and portions are from the food worksheet. Original logo artwork is extracted from the user's menu PDF. The hero is generated illustrative grill photography.

## Features

Food and drinks tabs; category filtering; case-insensitive and accent-insensitive search within the selected menu/category; prices by serving format; item detail dialog; persistent on-device favourites with clear all; deep links; phone links; responsive navigation; keyboard controls and reduced-motion support. The shortlist is not an online order.

No external requests, analytics, or fonts. No backend is required. Private access is enforced by Sites hosting; robots metadata is only an indexing hint.

## Editing

Update `dist/menu.json` for menu changes. Each item has a stable ID, group, category, name, prices, description and optional serving tag. Keep IDs stable to retain saved items. Deployment uses `.openai/hosting.json` with `dist` as the static directory.

## Redesigned experience

The second version replaces the original card grid presentation with a full-width food and bar hero, locally hosted display and editorial typography, photographic food cards, a category menu, a platter finder, and a persistent table list.

Guests can select serving formats, adjust quantities, view a running estimate, copy the table list, and save favourites. The table list is a browsing aid; orders go through the server. The platter finder uses the three source platters and menu serving sizes to suggest the least expensive combination covering 1–20 guests. Data and item IDs are unchanged.

New illustrative images were created with the built-in image generation tool: `dist/assets/wings.webp` (char-grilled wings on a dark plate), `dist/assets/fish.webp` (charcoal-grilled whole fish), and `dist/assets/bar.webp` (three unbranded drinks with blue accent lighting). The original logo and original platter hero image are retained. Font licence is included alongside self-hosted fonts.

### Validation

Desktop and mobile/tablet layouts were visually reviewed. Narrow layouts at 320px and 390px and the tablet layout at 820px have no document-level horizontal overflow. Browser checks covered hero switching, food/drinks tabs, category filtering, search and empty states, saved items, item detail dismissal, bottle selection, quantity changes, table totals, copied list content, reload persistence, removal, clearing, and group platter suggestions. Calculation checks included 1, 3, 4, 5, 6, 9 and 20 guests. All 88 source menu records and prices remain unchanged.

## Menu item photographs

All 88 menu items now have images. Web research supplied representative photos for the 83 items previously without pictures; duplicate items share the appropriate photo. Sourced images are hosted locally as optimized WebP assets. Thumbnails appear in menu rows, full photos appear in item details, and the table list uses the same images. Product photographs use `object-fit: contain` so the full bottle remains visible. `dist/menu-photos.json` preserves source URLs and applicable licence credits, which are displayed in item details. `IMAGE-SOURCES.md` lists the research sources.

Validation confirmed that all 88 menu IDs resolve to existing image assets, the original menu data and prices are unchanged, food and bottle photos open correctly, serving selection and table totals work, and 320px and 390px layouts have no horizontal overflow. Images outside the viewport load lazily.
