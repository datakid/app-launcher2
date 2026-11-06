# LinkExpress (revision 7)

Arabic and English launcher for 33 tools in four groups: Core, Tools, Experimental and Print. It previews a tool in a frame before opening it.

## What it does

- Lists 33 tools, 50 links counting variants, with search. `/` focuses the search box, Enter opens the selected tool, Tab and Space move through the list and Esc clears the search.
- Previews the selected tool in a sandboxed frame. When a site refuses to be framed, the page says so and offers Open in new tab and Retry.
- Pins tools, copies a tool's link, reloads the preview, and marks tools as new or closed.
- Switches between light and dark, between themes and between Arabic and English. A performance mode and a sound switch are in the settings.
- Keeps its settings and a cached copy of the tool list in `localStorage` (`linkexpress-prefs-v3`, `linkexpress-fihrist-v1`).

## What it does not do

- It does not host or run the tools. It frames each tool's own site, and a site that blocks framing opens only in a new tab.
- The tool list is embedded in `Index.html`. It tries to refresh the list from a `fihrist.json` next to the page, and keeps the embedded list when that file is missing or invalid. There is no `fihrist.json` in this repository.
- It has no accounts or sync.

## Network and install

Loads Google Fonts, requests each tool's site icon from Google's favicon service, and tries `fihrist.json` on its own site. A tool's own site loads when you preview it. Not installable; no service worker.

## Built with

One HTML file, with no build step, no framework and no libraries. The file is named `Index.html`, with a capital I.

## Run locally

Serve the folder with any static file server and open `/Index.html`.
