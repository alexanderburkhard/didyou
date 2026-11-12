# Did You? site

Static website for the iOS app Did You?: landing page (English and German), support, privacy policy and impressum. Plain HTML and CSS, no JavaScript, no third-party requests, system fonts. Public repo: nothing but the website belongs here, never app code.

| Page | Path |
|---|---|
| Landing (EN) | `index.html` |
| Landing (DE) | `de/index.html` |
| Support (EN, DE) | `support/index.html`, `de/support/index.html` |
| Privacy Policy | `privacy/index.html` (URL is linked from the App Store listing and the app) |
| Impressum | `impressum/index.html` (URL is linked from the app) |

- `style.css`: one stylesheet for every page. Colours are tokens on `:root` with a dark set under `prefers-color-scheme`. The coral bands and the charcoal ink come from the app.
- `img/`: the app icon and app screenshots (iPhone 17 simulator, `-demo`, light and dark, English and German) as WebP. The page picks the light or dark shot with `<picture>`.
- The notification copy on the landing pages is the real copy from the app's `CopyBook` and String Catalog. When it changes there, change it here.
- Support moved from `/` to `/support/`. The app's `Links.support` and `support_url.txt` in the store metadata still point at the site root, which is now the landing page.
- Preview locally: `python3 -m http.server` in this folder.
