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


SCANNER V3 — OPENCV LOADER FIX
------------------------------
The previous scanner could display "Engine Failed" simply because a 15-second
timeout expired while the large OpenCV.js library was still downloading.

This build:
- Removes that artificial timeout completely.
- Uses the official Emscripten Module.onRuntimeInitialized callback.
- Opens the camera immediately while OpenCV continues loading.
- Shows Engine "Loading" -> "Starting" -> "Ready".
- Only displays "Failed" when the actual script download fails.
- Starts page-edge detection automatically as soon as OpenCV reports ready.

FIRST-LAUNCH NOTE:
OpenCV.js is a large browser library. The first uncached iPhone load may take
noticeably longer than subsequent loads. Keep the scanner open until Engine
changes to Ready.
