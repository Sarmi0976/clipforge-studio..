# ClipForge Studio — Advanced Browser Video Editor

A responsive, single-page browser editor built with HTML, CSS and JavaScript. No build step is needed.

## Features
- Responsive UI for desktop and mobile browsers
- Import one video and one music/audio track
- Preview, play/pause, timeline seeking, trim start/end
- Text/title overlay with color, size and vertical position
- Visual filters: cinema, monochrome, warm, cool, vivid, faded
- Brightness and contrast controls
- Fade-in/fade-out transitions
- Export by recording the rendered canvas with mixed audio
- Video and audio files are selected locally; they are not uploaded to a server

## Run locally
Use a local HTTP server rather than opening the HTML file directly:
```bash
python -m http.server 8000
```
Then open `http://localhost:8000`.

Alternatively, with Node.js:
```bash
npx serve .
```

## Publish to GitHub Pages
1. Create a repository at https://github.com/new.
2. Upload `index.html` and this `README.md` to the repository root.
3. Open **Settings → Pages**.
4. Under **Build and deployment**, select **Deploy from a branch**.
5. Select branch `main`, folder `/ (root)`, and click **Save**.
6. Wait for the published URL to appear on the Pages screen, then test it in Chrome and another browser.

Other static hosting options include Netlify or Cloudflare Pages. This project has no server-side component.

## Export notes / limitations
- The editor records the canvas preview in real time. Export takes approximately as long as the selected clip plays.
- Output is WebM on most browsers. MP4 is used only if the browser supports MP4 recording through `MediaRecorder`; browser support varies.
- Keep the tab open and prevent the device from sleeping during export.
- Mobile browser memory and battery limits may constrain longer or high-resolution videos.
- This is a single-video-track starter: it is not a full CapCut replacement. There is one music track and one text overlay; no multi-clip transitions, keyframes, stickers, automatic captions, or undo history yet.
- Test your own source formats on the target browsers. Video playback/recording support varies by device and codec.
