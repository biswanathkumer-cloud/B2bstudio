# StudioPrint Pro — Browser-only Edition

This is a single-page photo editor. **No Python, no server, no installer, and no command prompt are required.**

## Start
1. Extract the ZIP file.
2. Double-click `index.html`.
3. Open it in the latest Google Chrome or Microsoft Edge.
4. Click **Add photos** or drag photos onto the editor.

## Features
- Multi-photo queue, undo/redo, rotate, flip, brightness, contrast, saturation, temperature and filters.
- Editable crop presets for passport, visa, PAN-style photo, signature and stamp sizes. These are convenience presets, not official validation.
- Browser-based AI background removal using Transformers.js + MODNet. The first run requires internet and downloads the model to the browser cache; subsequent use may reuse the cache. AI processing runs on the user's device.
- Solid-color keying, transparent-edge feathering, paint overlay layers, lasso selection, connected-pixel Magic Eraser.
- Gentle global skin smoothing/brightness controls (not face-aware/landmark retouch).
- KB/MB compression, PDF import/export (PDF libraries load from CDN), sheet print preview, batch passport printing.

## Important limitations
- Browser-only means images are edited in the current browser tab and are not uploaded to a server by this app. Clear the session or close the tab to clear the working session; browser caches may retain downloaded AI/PDF libraries, not your edited photo files.
- AI background removal and PDF tools require internet for the first library/model download. Browser/device memory and GPU capability affect performance. WebGPU is not required for MODNet CPU inference but a capable computer helps.
- Face retouch is global smoothing/brightening, not automatic face segmentation or professional face-aware retouch.
- Layers are paint-overlay layers. Applying destructive filters/crops may flatten the visible result.
- Hair edge feathering only softens existing transparent edges; it cannot restore missing hair strands.
- Lasso and Magic Eraser are pixel-based tools. Keep an original copy and use Undo to revert mistakes.
- Print size depends on printer settings. In the print dialog choose **Actual size / 100%** and disable Fit to page. Borderless/printable margins vary by printer and paper.
- PAN/NSDL/UTI requirements can change. Verify current official portal pixel dimensions, aspect ratio, format and file-size limits before submission.
- QR camera upload from another phone to the PC is intentionally not included: a phone-to-PC transfer requires a network receiver/server or an external cloud relay, which conflicts with the no-server/no-service requirement. Transfer the phone photo to the PC first, then open it here.

## Troubleshooting
- If AI background removal fails, use the latest Chrome/Edge, check internet, reload the page and retry. The first model download can be large and may take several minutes.
- If PDF import/export is unavailable, check internet access because PDF.js and jsPDF are loaded from a CDN.
- For best printing, use original high-resolution photos and the 300/600 DPI output option; printer driver settings still control the physical print.
