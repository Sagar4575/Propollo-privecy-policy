# Propollo — Legal Pages (Static Site)

Standalone static HTML pages for Propollo's legal documents. No build step, no
dependencies, no external requests. Host it directly with GitHub Pages.

## Files

| File          | Page                  | URL when hosted              |
| ------------- | --------------------- | ---------------------------- |
| `index.html`  | Privacy Policy        | `https://<user>.github.io/<repo>/` |
| `terms.html`  | Terms & Conditions    | `https://<user>.github.io/<repo>/terms.html` |
| `styles.css`  | Shared stylesheet (black & white) | —                  |
| `.nojekyll`   | Disables Jekyll on Pages | —                         |

## Publish with GitHub Pages

1. Push these files to the `main` branch of the repository.
2. Open the repository on GitHub → **Settings** → **Pages**.
3. Under **Build and deployment** → **Source**, choose **Deploy from a branch**.
4. Set **Branch** to `main` and the folder to **`/ (root)`**, then click **Save**.
5. Wait a minute or two; GitHub prints the live URL on the same page.

Every push to `main` republishes the site automatically. There is no workflow
to maintain.

### Custom domain (optional)

Add a `CNAME` file at the repo root containing only your domain, e.g.

```
legal.propollo.online
```

Then point a `CNAME` DNS record for that host at `<user>.github.io`, and enable
**Enforce HTTPS** in the Pages settings.

## Editing

- Text is plain HTML — edit `index.html` or `terms.html` directly.
- Both pages share `styles.css`. The palette is **strictly monochrome**
  (black, white, and greys) and switches between light and dark automatically
  based on the visitor's OS setting via `prefers-color-scheme`. Print styles are
  included.
- No logo, icon, or favicon is used anywhere on these pages.
- The pages currently use placeholder-free contact details:
  - Website: `https://propollo.online`
  - Email: `propollo.online@gmail.com`
- If you add a custom domain, update the `<link rel="canonical">` and
  `og:url` values in both HTML files.

## Notes

- `index.html` deliberately serves the **Privacy Policy** at the site root,
  because the repo name is `Propollo-privecy-policy` and this URL is typically
  what gets submitted to Google Play Console and OAuth consent screens.
- `terms.html` is the Terms & Conditions page, cross-linked from the Privacy
  Policy and vice versa.
- `.nojekyll` tells GitHub Pages to skip Jekyll processing.
