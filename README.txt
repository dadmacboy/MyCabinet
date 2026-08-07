FileNest — Zero-Cost Prototype v2
=================================

WHAT CHANGED
- Added a real browser-based document scanner mode.
- Detects the largest four-sided document edge using OpenCV.js.
- Draws a green outline around the detected document.
- Auto-captures once the document is large enough and stable.
- Perspective-corrects/crops the captured page.
- Manual Capture remains available as a fallback.
- Added Civic / Voter document type, including Voter Registration.
- Added explicit Save to Proton Drive, Save to Google Drive, Save to Files, and Share Elsewhere actions.
- Proton/Google buttons use the iPhone Share Sheet. FileNest renames the file first and tells you the suggested folder.

IMPORTANT IPHONE CAMERA REQUIREMENT
The scanner uses the browser camera API. Safari requires a secure HTTPS page for camera access.
Opening index.html directly from the iPhone Files app may allow the rest of the prototype to run, but camera scanning may not work.

Best free test method:
1. Put index.html on GitHub Pages or another free HTTPS static host.
2. Open the HTTPS link in Safari on the iPhone.
3. Allow Camera permission.
4. Tap Scan document.
5. Hold the document flat with all four edges visible.
6. A green outline should appear.
7. When stable, it auto-captures and perspective-corrects the page.

PROTON DRIVE / GOOGLE DRIVE
This version does not directly log into either service.
On iPhone:
1. Scan/choose the document.
2. Review filename and suggested folder.
3. Tap Save to Proton Drive or Save to Google Drive.
4. iOS Share Sheet opens with the renamed file.
5. Select Proton Drive or Google Drive.
6. Select/create the suggested folder.

That keeps the prototype at zero subscription/API cost and avoids storing credentials.

LIMITATIONS
- Scanned output is currently a corrected JPEG, not a multi-page PDF.
- One scanned page per filing action.
- Edge detection loads OpenCV.js from the free OpenCV CDN, so internet access is needed when the page loads.
- Browser-based apps cannot automatically navigate/create Proton Drive folders without a supported account integration.
- No OCR/document auto-classification yet.

NEXT LOGICAL TESTS
- How well edge detection works on your iPhone under normal lighting.
- Whether the Share Sheet shows Proton Drive and Google Drive reliably.
- Whether suggested categories/questions feel natural.
- Then add multi-page scan-to-PDF and local OCR.
