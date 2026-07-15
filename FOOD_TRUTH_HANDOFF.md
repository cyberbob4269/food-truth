# Food Truth App Handoff

This note is for the next Codex chat. It is intentionally about the Food Truth app only. Do not bring forward the browser troubleshooting notes unless Scott explicitly asks.

## Project Location

- Current working project: `C:\Users\TSLA BoT\Documents\Food truth app`
- Main app file Scott opens: `C:\Users\TSLA BoT\Documents\Food truth app\index.html`
- Supporting material: `C:\Users\TSLA BoT\Documents\Food truth app\FoodTruth`
- Do not touch the old folder `C:\Users\Vera-at-home\Desktop\OpenClaw\FoodTruth` unless Scott explicitly asks. That earlier location caused confusion.

## What This App Is

Food Truth is a UK supermarket food/product truth app. The aim is to help people quickly see:

- what is good to buy
- what is bad or misleading
- what additives, processing tricks, welfare issues, or branding tricks are involved
- better alternatives in mainstream UK supermarkets

The tone is direct, consumer-facing, and opinionated. Keep claims useful and readable, but tighten sourcing as the project grows.

## Current App Shape

`index.html` is a static single-page app with embedded CSS, JavaScript, and product data.

The visible product data currently lives in the JavaScript array:

- `const CATS = [` starts around line 128 in `index.html`
- each category has `id`, `name`, `emoji`, and `products`
- each product generally has fields such as `id`, `v`, `name`, `brand`, `store`, `reason`, `alts`, `hl`, `warn`, `price`, and `rating`
- `v` is the verdict, commonly `avoid` or `buy`

Current categories in the live app:

- Eggs
- Butter
- Meat
- Bread
- Emulsifier Watch

The folder `FoodTruth\data\products.json` contains a structured JSON version of the product data. The folder `FoodTruth\content` contains category research markdown files:

- `bread-uk-supermarkets.md`
- `butter-uk-supermarkets.md`
- `eggs-uk-supermarkets.md`
- `emulsifiers-uk-supermarkets.md`
- `meat-uk-supermarkets.md`

Use those files as source material when expanding or checking the app.

## Cleanliness Notes

Before this handoff file was added, the project root contained only:

- `index.html`
- `FoodTruth\`

Browser troubleshooting and reinstall helper files were cleaned out. Keep this folder focused on the Food Truth app. If temporary scripts or logs are needed, remove them afterwards or put them somewhere clearly temporary.

## Running / Viewing

Scott currently uses `index.html` directly in a browser.

If a local server becomes useful later:

- do not kill or take over ports that are already in use
- check whether a port is free first
- if the usual port is occupied, pick a different free port and tell Scott which one
- prefer `127.0.0.1:<port>` for local browser testing

## Next Useful Work

Good next steps for a fresh chat:

- add more UK supermarket products and categories
- add source URLs or citation fields for factual claims
- add search/filter by supermarket, additive, product category, verdict, and keyword
- consider moving live app data out of `index.html` and into JSON once the data grows
- review any strong health-risk claims before publishing, especially percentage-risk statements and additive/illness links
- make sure the app remains quick to open and useful on mobile

## Scott's Project Preferences

- Keep changes scoped and visible.
- Do not edit unrelated files.
- Do not reintroduce browser bug-reporting material into this project.
- Treat `C:\Users\TSLA BoT\Documents\Food truth app\index.html` as the source of truth unless Scott says otherwise.
