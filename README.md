# SMotion Studio (Web Beta)

A free, no-ad, browser-based editing prototype designed to deploy as a static site on **GitHub Pages**. It uses plain HTML, CSS and JavaScript—no build step, package manager, API key, or paid service required for the basic editor.

## Included in this package

- Import videos, photos and audio from your device; drag and drop is supported.
- Preview canvas with crop/fit, aspect ratio, rotation, flip, zoom, opacity, speed, volume, color adjustments and several filter/effect presets.
- Timeline clip selection, trim in/out points, split, duplicate, replace, delete, play/pause and scrubbing.
- Text overlay, emoji stickers, image overlays, editable starter templates, manually timed captions and SRT export.
- Browser-native real-time export to WebM where supported (MP4 only where the browser reports compatible MediaRecorder support), plus PNG export of a cover/current frame.
- Audio extraction to WebM where supported by the browser, a selected audio bed for preview/export, and basic amplitude-based beat markers.
- Local project persistence using IndexedDB, local display profile, XML project-metadata export and JSON metadata export.
- Responsive layout for desktop and mobile screens.

## Deploy to GitHub Pages

1. Download and extract this ZIP.
2. Create a public GitHub repository, for example `smotion-web`.
3. Upload **the contents** of the `SMotion` folder to the repository root. `index.html`, `style.css`, `app.js`, `README.md`, `.nojekyll`, and the `assets/` folder should sit at the root (do not upload only the outer folder).
4. In the repository, open **Settings → Pages**.
5. Under **Build and deployment**, choose **Deploy from a branch**, select your branch (usually `main`) and folder `/ (root)`, then Save.
6. Open the published Pages URL after GitHub finishes deployment. Use HTTPS for media APIs and browser storage.

## Important scope notes

This is an **MVP/working prototype**, not a complete replacement for CapCut or a native nonlinear editor. Export records the canvas in real time, so long clips take at least as long as their playback duration and can be demanding on mobile devices. Codec/container support varies by browser. Export targets the selected clip/trim segment rather than rendering a multi-clip sequence into one continuous movie. XML/JSON exports are edit metadata, not rendered video and do not embed the source media.

Some controls are intentionally limited or labeled as not implemented in this MVP: true reverse playback/rendering, optical-flow smooth slow motion, a full 150+ effect marketplace, advanced keyframe interpolation/graph editor, chroma-key background removal, AI retouch/auto captions/auto cut, vector drawing UI, nested parent composition, and a production-ready account/Google sign-in service. Those need a more substantial rendering engine, ML models, or OAuth/backend configuration. The “Freeze” action in this MVP freezes the preview frame; it does not create a separate hold-frame timeline segment.

## Local privacy and projects

Media is processed in the browser and is not uploaded to an SMotion server. Project save uses IndexedDB on the current browser/device. Browser site-data clearing, private browsing, storage limits, or switching devices can remove saved projects. Keep original media and exported files backed up separately. The local profile is only a display name; Google sign-in is not configured.

## Supported formats

The file picker accepts common browser formats including MP4/WebM/MOV, PNG/JPEG/WebP, and MP3/WAV/OGG/M4A. Actual codec support is determined by your device and browser. If a particular file will not play, convert it to H.264/AAC MP4 or WebM and retry.

## License

Use and modify this starter project freely for personal projects. Third-party codecs, browser APIs, and any future added libraries remain subject to their own licenses.
