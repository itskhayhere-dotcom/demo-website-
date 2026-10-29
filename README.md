# Mido Scroll Experience

Scroll-driven video page. The background video plays forward and backward as you scroll.

## Files
- `index.html` - the whole page (HTML, CSS, JS)
- `assets/mido-scroll.mp4` - background video (muted, short keyframe gaps so scrubbing stays smooth)

## Run locally
The video needs a server that supports HTTP Range requests, or the browser cannot seek and the video will not move.
Use one of these:

    npx http-server -p 8000

or the VS Code "Live Server" extension. Then open http://localhost:8000

Do NOT use `python3 -m http.server`. It has no Range support, so the video will not play on scroll.
Double-clicking `index.html` may also fail in some browsers.

## Deploy with GitHub Pages
1. Push this folder to a GitHub repo.
2. Repo Settings > Pages > Deploy from a branch > `main` / root.
3. Your site goes live at `https://<username>.github.io/<repo>/`.

## Notes
- Keep the video at a low bitrate and a short keyframe interval. A normal video will scrub with lag.
- On iPhone the video starts scrubbing after the first touch.
