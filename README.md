# Recipe Box

A simple, Paprika-style recipe manager that runs entirely in your browser. One file (`index.html`), no server, no build step.

## Features

- **Browser import**: a "Save to Recipe Box" bookmark that pulls the recipe from the page you are on (works with most recipe sites, which publish schema.org recipe data).
- **Paste import**: paste page source, recipe JSON, or plain text.
- **Web address import** (optional): needs a CORS proxy prefix, set under Import > Proxy settings.
- **Add and edit** recipes: title, photo, servings, prep and cook time, source link, tags, ingredients, directions, notes.
- **Photos**: upload or drag in a photo (resized to 1200 px), or paste an image address.
- **Tags**: add tags to any recipe and filter the list by one or more tags (recipes must have all selected tags).
- **Search** across titles, ingredients and tags.
- **Backup and restore** as a JSON file.

## Publish on GitHub Pages

1. Create a new repository on GitHub, for example `recipe-box`.
2. Upload `index.html` (and this README) to the root of the `main` branch.
3. Go to **Settings > Pages**, set **Source** to *Deploy from a branch*, choose `main` and `/ (root)`, then **Save**.
4. After a minute or two the app is live at `https://<your-username>.github.io/recipe-box/`.

## Set up the browser import

1. Open your live GitHub Pages address and go to **Import**.
2. Drag the red **Save to Recipe Box** button onto your bookmarks bar.
3. On any recipe page, click the bookmark. The recipe opens in Recipe Box for you to check and save.

Set the bookmark up from the live address, as it remembers which address to send recipes to. On iPhone or Android, use **Copy bookmarklet code**, create any bookmark, then edit it and paste the code in as its address.

## Where your data lives

Recipes are stored in your browser (IndexedDB), not on GitHub, so each browser and device keeps its own collection. Use **Backup** to download a file and **Restore** to load it elsewhere. Clearing your browser's site data deletes the recipes, so keep a backup.

The imported recipe travels in the part of the address after `#`, which browsers never send to any server.
