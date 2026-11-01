# Knuckle Sandwich ✊

A small, single-file web app: take or upload a photo of your fist, build a sandwich around it
(bread, toppings, sauces), name it, and send it to someone who deserves a bite.

**Live demo:** `https://<your-username>.github.io/knuckle-sandwich/` (after enabling GitHub Pages, see below)

## Features

- Photo step with camera capture or upload, automatic background cutout and lighting boost, adjustable tolerance and tap-to-fix
- Sandwich builder: 6 breads, 9 toppings, 10 sauces, grilled finish, drag-and-drop or tap
- Recipe card with recipient, reason, message and an auto-growing "price you're demanding" field
- Place order saves an image and opens your Messages app (with a number) or the share sheet (without one)
- No build step, no dependencies, no backend

## Run locally

Open `index.html` in a browser. For the camera, serve it over `localhost` or HTTPS:

```bash
python3 -m http.server 8000
# then visit http://localhost:8000
```

## Deploy to GitHub Pages

1. Push this repo to GitHub.
2. Go to **Settings → Pages** and set **Source** to **GitHub Actions**.
3. Push to `main`. The included workflow publishes the site.

## Privacy

Photos are processed entirely in your browser on a canvas. Nothing is uploaded or stored.

## Project layout

```
index.html                    the whole app (HTML, CSS, JS, embedded logo images)
.github/workflows/pages.yml   GitHub Pages deploy
LICENSE                       MIT
```

## Notes

- Fonts (Bowlby One, DM Sans) load from Google Fonts, with system fallbacks.
- Browsers can't send a text silently, so the final Send tap in Messages is yours.

## License

MIT, see [LICENSE](LICENSE).
