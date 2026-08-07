FileNest — FINAL replacement package
====================================

MAIN FILE
- Use index.html as the app.
- This replaces the prior FileNest_v3.html file.
- If you are updating an existing static host/repository, delete the old HTML file after index.html is uploaded and confirmed working.

IPHONE ICON
- apple-touch-icon.png is used by Safari Add to Home Screen.
- filenest-icon-1024.png is the full-size icon for Shortcuts/manual icon selection.
- Keep all files from this ZIP in the same folder.

IMPORTANT
- Camera scanning still requires HTTPS in Safari/Chrome.
- If you open index.html directly from Files, basic app functions may work, but camera access can be blocked by iOS.
- For the phone shortcut/Home Screen app, host this folder on the same HTTPS site you were using before.

REPLACEMENT STEPS
1. Extract this ZIP.
2. Upload index.html and all included icon/manifest files to the same folder on your host.
3. Confirm the FileNest page opens.
4. Delete the older FileNest_v3.html/index file only after the new page works.
5. On iPhone, remove the old Home Screen shortcut if necessary and add FileNest again so iOS refreshes the icon.


SCANNER V2 — EDGE ENGINE REBUILD
--------------------------------
This build rebuilds the document scanner around reliable OpenCV.js initialization.

Visible scanner diagnostics:
- Engine: Loading / Ready / Failed / Error
- Edges: number of four-corner page candidates detected
- Stable: progress toward automatic capture (0/8 through 8/8)

Detection improvements:
- Handles OpenCV.js builds where cv initializes asynchronously or as a Promise.
- CLAHE contrast enhancement for uneven light/shadows.
- Lower Canny thresholds for softer paper edges.
- Morphological closing to reconnect broken page borders.
- Tests several polygon-approximation tolerances.
- Scores candidates by size, rectangularity, and center position.
- Draws green corner dots and a green quadrilateral when a page is found.
- Auto captures only after eight stable detection frames.
- Manual Capture still works if OpenCV fails.

PHONE TEST:
1. Replace the hosted index.html with this build.
2. Force-refresh Safari or remove/re-add the Home Screen shortcut to avoid cached JavaScript.
3. Open scanner.
4. Engine should change from Loading to Ready.
5. Point at a sheet of paper with contrasting background.
6. Edges should increase above 0 and a green outline/corner dots should appear.
7. Hold still until Stable reaches 8/8; auto capture should fire.
