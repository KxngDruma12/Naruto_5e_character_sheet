# Shinobi Foundry — Naruto Tabletop Character Creator

A responsive, offline-first character creator for the user's Naruto tabletop RPG ruleset.

## Run locally

- Open `index.html` in a modern browser, or
- From this folder run `python3 -m http.server 8080` and visit `http://localhost:8080`.

No build step, package manager, external CDN, or internet connection is required.

## Included in this first working version

- Character identity and background fields
- Catalogs for the 44 clan entries and 11 main classes
- Manual ability score entry with live modifiers
- Editable class hit die, chakra die, level-1 HP base and chakra base
- Automatic HP, Chakra, proficiency, AC and initiative calculations
- Clan feature browser with selectable features and full descriptions
- Full clan-jutsu library: 418 techniques across 39 clan lists, with rank, costs, components, keywords, prerequisites and complete descriptions where provided by the source
- Clan traits and lineage details displayed separately from feature descriptions
- Searchable clan-jutsu selector with one-click add to the character sheet
- Jutsu, features and inventory lists
- Local browser save, JSON export/import, and print / Save as PDF
- Responsive layout for desktop and mobile

## Rules integrity notes

This remains a partial rules engine, but the clan reference is now source-populated. The clan browser includes all 44 clan entries, 230 named feature headings, and 418 clan jutsu across the 39 clans that have separate clan-jutsu lists in Tsunade’s Studies Compendium. Hatake, Hoshigaki, Kurama, Sarutobi and Shí Hóu do not have separate clan-jutsu lists in that compendium; the site reports that rather than inventing techniques. It intentionally does not auto-apply recommended clan ability-score increases, assume a point-buy budget, certify jutsu prerequisites, or invent class-specific values. Enter class hit die, chakra die, level-1 HP base, chakra base, armor bonus, and feature text from the relevant source entry. The default proficiency progression and base AC formula follow the core Naruto 5E character rules surfaced in the supplied rules material. Confirm all selections against the current compendiums before play.

Clan feature descriptions and clan jutsu are transcribed from Tsunade’s Studies Compendium; line wrapping is normalized for screen display. Jutsu are added to a character sheet as selected entries only. The creator does not automatically grant them or certify their rank, prerequisites, affinities, clan ability point purchases, or character-level access.

The clan and class catalogs are separated correctly: Non-Clan, Bloodline Latents and Legacy Content are not listed as clans; class specializations are recorded separately from the 11 main classes.

## Local and online use

The same static site can be opened locally or hosted on any static web host. Character saves are currently stored in the browser's local storage and can be transferred with JSON export/import. This initial build does not yet include user accounts or cloud synchronization; those require a backend and a chosen hosting/database provider. No deployment or external account was created.

When hosted over HTTPS (or localhost), the included service worker caches the app shell for offline revisits and the manifest allows installation as a browser app. Browser local storage remains device/browser-specific; use JSON export to move characters between devices.
