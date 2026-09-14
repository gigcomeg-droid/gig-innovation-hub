# GIG-Egypt Technology & Innovation Hub — presentation website

A single-page, scroll-based presentation site. Seven sections. The text follows the deck word for word, apart from the proofreading
corrections listed under **Copy** below.

## What's in this folder

| File | What it is | Required |
|---|---|---|
| `index.html` | The whole site — HTML, CSS and JavaScript in one file | Yes |
| `gig-logo.png` | GIG-Egypt logo (white version), used in the header and on the closing section | Yes |
| `gig-shell.png` | GIG shell mark, used as the ambient brand graphic | Yes |
| `GIG-Egypt-Technology-and-Innovation-Hub.pdf` | Print edition — 8 pages, A4 landscape | No — not part of the site |
| `print-source/` | The HTML the PDF is generated from, if you ever need to re-export | No — not part of the site |
| `README.md` | This guide | No — do not upload |

Keep `index.html`, `gig-logo.png` and `gig-shell.png` **in the same folder**. The page looks
for both images next to itself, so if you move the HTML without them they will not appear.

### Copy

All wording on both the site and the PDF is the approved copy supplied by GIG-Egypt
(revision of 14 September 2026). The earlier PowerPoint wording has been replaced
throughout; the Cairo ICT section was removed and its quotation moved onto the
Innovation System section.

### Colour

Every colour on the site comes from the GIG Brand & Identity Guidelines: Indigo #19058C,
Deep Blue #1F0F4D, Pearl #E5E5E5, Rose-Gold #D28C64, Ocean #8094E6, Sunrise #FF7366,
Seafoam #6BCABA and white, plus tints and shades of Indigo and Deep Blue for depth.
They are declared once as CSS variables at the top of `index.html` under `:root`.

## The print edition

`GIG-Egypt-Technology-and-Innovation-Hub.pdf` is the same seven sections laid out for paper:
A4 landscape, one section per page, in a light treatment — white and Pearl ground with
Indigo type and Rose-Gold accents, the second background option in the guidelines. It uses
a fraction of the ink of the on-screen version and photocopies cleanly. The text is
selectable and searchable, not a picture of the page.

To re-export after editing: open `print-source/print.html` in Chrome, press Ctrl+P
(Cmd+P on a Mac), choose **Save as PDF**, set Layout to **Landscape**, Paper size to
**A4**, Margins to **None**, and tick **Background graphics**.

## Test it before uploading

Double-click `index.html`. It opens in your browser and works exactly as it will online.

## How to publish it

### Option 1 — Your company web server / intranet (IT team)

1. Send `index.html` and `gig-logo.png` to whoever manages the web server.
2. Ask them to place all three files in the same folder, for example
   `/innovation-hub/`.
3. The address becomes `https://yourdomain.com/innovation-hub/`.
   A folder containing `index.html` opens automatically — no file name needed in the URL.

### Option 2 — Netlify Drop (fastest, free, no account needed to start)

1. Put `index.html`, `gig-logo.png` and `gig-shell.png` together in one folder on your computer
   (do **not** include `README.md`).
2. Go to **https://app.netlify.com/drop**
3. Drag that folder onto the page.
4. Wait a few seconds. You get a live link like `https://random-name.netlify.app`.
5. Create a free account when prompted if you want to keep the link permanently,
   rename it, or connect your own domain.

### Option 3 — SharePoint / OneDrive

SharePoint often blocks HTML pages from running scripts, so animations may not work.
If your IT team allows it:

1. Upload all three files to the same document library folder.
2. Open `index.html` and choose the option to view in the browser.

If it downloads the file instead of opening it, use Option 1 or 2 instead.

### Option 4 — GitHub Pages (free, permanent)

1. Create a repository at **https://github.com/new** and tick "Add a README file".
2. Click **Add file → Upload files**, drag in `index.html`, `gig-logo.png` and `gig-shell.png`, then **Commit changes**.
3. Go to **Settings → Pages**.
4. Under "Build and deployment", set Source to **Deploy from a branch**,
   branch **main**, folder **/ (root)**, then **Save**.
5. Wait 1–2 minutes. Your link appears at the top of that same Pages screen,
   in the form `https://yourname.github.io/repository-name/`.

## Editing the content later

Open `index.html` in any text editor (Notepad, VS Code) and search for the sentence you
want to change. Section 1 to 8 are marked with comments like
`<!-- ==================== 3 · EIGHT STAGES ==================== -->`.

The eight stages, the evaluation weightings, the recognition cards and the pipeline steps
are stored as lists near the top of the script, under the comment
`/* ---------- DATA (verbatim from source deck) ---------- */`. Editing them there updates
both the diagram and the text.

## Presenting it

- **Scroll** or press **↓ / ↑**, **Page Down / Page Up**, or **Space** to move between sections.
- Press **1** to **8** to jump straight to a section.
- **Home** goes to the title, **End** to the closing section.
- The top menu and the markers on the right also jump between sections.
- Press **F11** for full screen while presenting (Windows), or **Ctrl+Cmd+F** on a Mac.

## One note about animations

The motion uses the GSAP animation library, loaded from a public address (cdnjs.cloudflare.com)
in the first lines of `index.html`. If your corporate network blocks that address, the site
still works and every word stays readable — the animations simply appear finished instead of
playing. To make them work behind a strict firewall, download `gsap.min.js` from
`https://cdnjs.cloudflare.com/ajax/libs/gsap/3.12.5/gsap.min.js`, put it next to `index.html`,
and change that line to `<script src="gsap.min.js"></script>`.
