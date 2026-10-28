# Hosting One Band Works

The site is plain HTML, CSS and JavaScript. There is no build step: the files in this repo are the deployable build.

## Preview (now)

GitHub Pages serves the `main` branch at:

- Picker: https://chasetheworld14-prog.github.io/One-band-works-site/
- Living Hive: https://chasetheworld14-prog.github.io/One-band-works-site/living-hive/

Every push to `main` updates the preview in about a minute.

## Living Hive routes

| Route | What it shows |
| --- | --- |
| `#/aerial` | Exterior hive, welcome card |
| `#/bridge` | Golden bridge |
| `#/entrance` | Portal gate |
| `#/atrium` | Interior atrium with six chamber doors |
| `#/chamber/people`, `systems`, `technology`, `opportunity`, `solutions`, `resources` | Chamber sheets |
| `#/contact` | Talk to the Hive note builder |

The Menu button lists every route as a plain link, so the site can be navigated even if the animated scene fails to draw.

## Pointing onebandworks.com here (only after approval)

1. GitHub: repo **Settings → Pages → Custom domain**, enter `onebandworks.com`, click **Save**.
2. Namecheap: **Domain List → Manage → Advanced DNS**, then add:
   - `A Record`, Host `@`, Value `185.199.108.153`
   - `A Record`, Host `@`, Value `185.199.109.153`
   - `A Record`, Host `@`, Value `185.199.110.153`
   - `A Record`, Host `@`, Value `185.199.111.153`
   - `CNAME Record`, Host `www`, Value `chasetheworld14-prog.github.io.`
   Leave the two TXT records (SPF and DMARC) in place.
3. Wait for DNS (minutes to a few hours), then tick **Enforce HTTPS** in GitHub Pages settings.
4. Decide which page is the homepage: the root `index.html` is currently the preview picker. Swap in the chosen design before going live.
