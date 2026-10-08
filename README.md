# foundational.bio release package

Copy everything in this folder into the root of the website repository, replacing existing files, then commit and push. GitHub Pages serves index.html at the root.

## Files

- index.html: the full site, self-contained (images and fonts inlined); includes canonical URL, Open Graph and Twitter cards, and Organization JSON-LD
- og-image.png: social share image (1200x630), referenced as https://foundational.bio/og-image.png
- favicon.ico, favicon.svg, favicon-32.png, favicon.png, apple-touch-icon.png, icon-512.png: site icons
- site.webmanifest: web app manifest (icons, theme color)
- robots.txt: allows all crawlers and points to the sitemap
- sitemap.xml: single-page sitemap
- llms.txt: plain-text company summary for AI assistants, served at https://foundational.bio/llms.txt

## Notes

- Share-card tags (Open Graph, Twitter, description, canonical) are written as static HTML in the head of index.html so Slack, LinkedIn, and X can read them without running JavaScript.
- After deploying, Slack caches link previews for a while. To force a refresh, paste the URL with a query string (https://foundational.bio/?v=2) or wait for the cache to expire.
- Keep the existing CNAME file (custom domain) if the repo has one.
- The quote form posts to HubSpot (portal 243505211). Last Name must not be required on the HubSpot form, or single-word names will be rejected.
- Update the lastmod date in sitemap.xml when you ship content changes.

## After deploying

1. Open https://foundational.bio and confirm the favicon and hero load.
2. Check the share card with the LinkedIn Post Inspector and the X card validator.
3. Send one test form submission and confirm it lands in HubSpot.
4. Submit https://foundational.bio/sitemap.xml in Google Search Console.
