# 🥪 Knuckle Sandwich

Build a sandwich around a photo of your fist and send it to someone who deserves a bite.

**Live demo:** `https://YOUR-USERNAME.github.io/YOUR-REPO/` (after you enable GitHub Pages, see below)

## How it works

1. **Photo.** Take a picture of your fist with the camera, or upload one.
2. **Enhance.** The fist is found and cut out automatically, then the lighting is boosted. You can tap or brush away anything that was missed.
3. **Build.** Pick a bread, toppings and sauces, name the sandwich, and fill in who it's for and why.
4. **Send.** Save or share the finished image, or text it.

Everything runs in your browser. Photos are never uploaded to a server.

## Run it

It is one file with no build step.

- **Locally:** open `index.html` in a browser. (The camera needs HTTPS or `localhost`, so for camera testing run `python3 -m http.server` in this folder and visit `http://localhost:8000`.)
- **GitHub Pages:**
  1. Push this folder to a GitHub repository.
  2. Go to **Settings → Pages**.
  3. Under **Build and deployment**, choose **Deploy from a branch**, pick `main` and `/ (root)`, then **Save**.
  4. After a minute your site is live at the link shown on that page.

## What loads from the internet

| What | From | Why |
| --- | --- | --- |
| Bowlby One + DM Sans fonts | Google Fonts | Look of the page and the saved image |
| MediaPipe tasks-vision `0.10.14` | jsDelivr | Automatic fist detection |
| `hand_landmarker.task` model | Google storage | Automatic fist detection |

The detection files only download when someone reaches the Photo step. If they can't load (offline, blocked), the app falls back to a colour-based background cutout and still works.

## Files

| File | Purpose |
| --- | --- |
| `index.html` | The whole app (HTML, CSS, JavaScript and embedded logos) |
| `.nojekyll` | Tells GitHub Pages to serve the file as-is |
| `README.md` | This file |
| `LICENSE` | MIT license |

## Tips for the best cutout

- Plain, lightly coloured background and good light.
- Knuckles toward the lens, fingers curled into a tight fist.
- Line the fist up with the dotted outline. It turns green when a fist is recognised.

## Browser support

Current Chrome, Edge, Safari and Firefox on desktop and mobile.
