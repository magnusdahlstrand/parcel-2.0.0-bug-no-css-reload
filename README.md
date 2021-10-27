# Parcel v2.0.0 CSS reload bug

## Issue

Automatic reloading of CSS does not work with 2.0.0, but does work with 2.0.0-rc.0.

## How to run

Please note that removing `.parcel-cache` after downgrading to `rc.0` seems to be required to get it back to working after having a broken install.

### Working version (`2.0.0-rc.0`)

```
git checkout main
npm install
npm run dev
```
1. Open in browser.
2. Edit `~/src/App.css`, change the colour of the div.
3. The browser will show the newly selected colour.

### Broken version (`2.0.0`)

```
git checkout broken
npm install
npm run dev
```
1. Open in browser.
2. Edit `~/src/App.css`, change the colour of the div.
3. The browser will show the old colour, and a manual page reload is required to see changes.
