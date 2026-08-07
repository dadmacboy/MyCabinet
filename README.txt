FileNest — Native Scanner build
================================

THIS BUILD DOES NOT USE OPENCV OR ANY COMPUTER-VISION CDN.

The document scanner is implemented inside index.html using browser JavaScript:
- live rear-camera preview
- grayscale + Sobel edge detection
- adaptive edge threshold
- edge dilation to join broken page borders
- connected-component page-outline search
- four-corner estimation
- green quadrilateral + corner markers
- 6-frame stability lock
- automatic capture
- native perspective correction
- Review Scan screen with Retake / Use Scan
- manual Capture fallback

TESTING
1. Upload ALL files from this ZIP to the GitHub repository root.
2. Wait for GitHub Pages to redeploy.
3. First test the GitHub Pages URL directly in Safari, not the old Home Screen shortcut.
4. Tap Scan document.
5. Rear camera should open immediately.
6. Put a white/bright sheet on a contrasting darker background.
7. Green corners and border should appear when the page is found.
8. Hold still until Stable reaches 6/6.
9. FileNest should auto-snap and show Review Scan.
10. Tap Use Scan or Retake.

There is no "Engine Loading" stage in this version because the detector is built into the page.
