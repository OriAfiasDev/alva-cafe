# עלווה קפה – ALVA (demo)

**A fictional business.** This is a design/tech demo of a scrollytelling site for a
coffee cart: the brand, the name, the address, the phone numbers, the social
handles, the opening hours and every one of the reviews are invented. Nothing
here describes a real place, and the page is served with `noindex`.

Hand-built static HTML/CSS/JS, RTL Hebrew, a scroll-scrubbed hero video whose
giant type lands in step with the desserts being set on the board and closes into
the name — no framework, no build step.

Live: https://oriafiasdev.github.io/alva-cafe/ (GitHub Pages, `main`, root).

## Local preview

```bash
python3 serve.py 8767
```

then open `http://localhost:8767`. (`serve.py` adds HTTP Range support, which
the hero `<video>` needs — Safari refuses to load a video without it.)

## Structure

- `index.html` — markup, JSON-LD, all copy
- `assets/css/style.css` — palette/scale as custom properties, every section
- `assets/js/main.js` — hero scrub + type choreography (six words land with the
  hands, then "עלווה"/"קפה" close into the name), pinned menu strip that pans
  with vertical scroll, word reveal, stream steps (pinned photo on desktop, one
  photo per step on phones), staged reviews on phones, nav state
- `assets/video/` — `hero.mp4` (1280×720, short GOP for scrubbing) and
  `hero-sm.mp4` (4:3 centre crop for phones)
- `assets/img/` — poster frames, logo, `photos/` stock photography

Source video (`hero.mp4` at the root) and `brief.md` are git-ignored.

## Credits

- Photography: [Unsplash](https://unsplash.com), used under the
  [Unsplash License](https://unsplash.com/license) (free to use, no permission or
  attribution required — credited here anyway).
- Type: [Karantina](https://fonts.google.com/specimen/Karantina) and
  [Alef](https://fonts.google.com/specimen/Alef) via Google Fonts (OFL).
- Logo and favicon: drawn for this demo as inline SVG.
