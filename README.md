# AR overlay demo

Point your camera at `logo2.jpg` to see `site_preview.png` locked on top using OpenCV.js feature tracking.

## Run locally
1. Serve the folder (any static server works):
   - `python3 -m http.server 8000`
   - or `npx serve .`
2. Open the page (for http.server): http://localhost:8000/index.html
3. Click **Start camera**, allow camera access, then show `logo2.jpg` (printed or on screen) in view.

Tips: good light, keep the full logo in frame, and hold steady for the lock. Internet is required to load `opencv.js` from the CDN.
