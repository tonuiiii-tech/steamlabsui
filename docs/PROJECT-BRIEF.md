# Project brief

The one-page record of why steamlabsui exists and who it is for. Fields marked **TBC** are still to be confirmed by the project owner.

| Field | Value |
|---|---|
| Project name | steamlabsui (STEAMLabs Africa standard UI kit) |
| Project ID | **TBC** |
| Project sponsor | **TBC** |
| Maintainer | Enock (`tonuiiii-tech`) |
| Repository | `steamlabsui`, published to npm as `steamlabsui` |
| Logged | 2026-10-29 |

## Target users

- **STEAMLabs developers** building the company's React apps: the website (`STEAMLabs_official_website`), Forms (`steam-forms`), the SLAP workspace app, the educators site (`African-educators`) and the LMS (`steamlabslms`).
- **Developers on non-React pages** (HTML, Vue, Svelte, email templates), who use the plain `.sla-*` classes and CSS tokens.
- **Designers and content owners** who need every product to follow the Brand Manual 2026 and the five program themes (`academy`, `elevate`, `showcase`, `nextgen`, `educators`).
- **End users of those apps** (learners, educators, partners and staff), who get one consistent and accessible interface.

## Problem statement

Each STEAMLabs app built its own UI. The 2026-10-11 scan in [INVENTORY.md](INVENTORY.md) found the same components rebuilt in up to five repos (for example `Button` in the website, Forms, educators, LMS and SLAP), each styled differently: SLAP used Tailwind's slate and indigo palette and Forms used tinted brand colours, both against the Brand Manual's full-strength rule. The result is duplicated work, drift from the brand, uneven accessibility and a slower path to every new screen. steamlabsui replaces those copies with one tested package of tokens, CSS and React components that every app imports.

## Current manual workarounds

- **Copy and paste between repos.** Developers copy a component from another app and restyle it, so fixes made in one app never reach the others.
- **Brand values typed by hand.** Colours, fonts and spacing are copied from the Brand Manual into each app's CSS, and the Manual's RGB values disagree with its own hex codes, so apps can end up with different greens.
- **Program themes rebuilt per app.** The program accent colours live in the website's `client/styles.css` and are recreated elsewhere.
- **Heavy UI dependencies per app.** Apps pull in Radix-based kits for dialogs, menus and accordions where native HTML would do.
- **No published package yet.** Until steamlabsui is on npm, apps install a tarball built with `npm pack` (see [PUBLISHING.md](PUBLISHING.md)).

## Open questions for the owner

1. What is the project ID?
2. Who is the project sponsor?
