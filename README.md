# NINELIJ — CMS-ready tattoo flash site

This version is built to be edited visually with Pages CMS.

## What you edit in the CMS
- Flash image
- Flash name/reference
- Category
- Available / claimed / repeatable status
- Description
- Any number of sizes and prices
- Homepage titles and copy
- Instagram / Tally / Calendly / Qonto / email links

## One-time setup
1. Create a GitHub repository and upload everything in this folder to the repository root.
2. In GitHub repository Settings → Pages, deploy from the `main` branch and `/ (root)` folder.
3. Go to https://app.pagescms.org and sign in with GitHub.
4. Install/authorize Pages CMS for the repository when prompted.
5. Open the repository. Pages CMS will read `.pages.yml` automatically.
6. Edit `Site settings` or `Flashes`, upload images, and save.

Pages CMS writes changes directly to the GitHub repository. GitHub Pages then serves the updated static site.

## Site files
- `index.html` — design/layout
- `app.js` — behaviour
- `data/site.json` — editable site texts + links
- `data/flashes.json` — editable flash catalogue
- `images/` — uploaded flash images
- `.pages.yml` — visual editor configuration
- `admin.html` — shortcut page to the editor

## Notes
The `Book this flash` button uses your `bookingUrl` from Site settings and adds tracking parameters containing the flash reference and selected size. Configure the post-booking redirect inside your booking service to send clients to your Qonto deposit link if desired.
