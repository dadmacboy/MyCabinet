SMART FILE CABINET — TEST PROTOTYPE

What it does
- Uses your phone camera or file picker
- Asks category-specific questions
- Generates a folder and filename
- Downloads a renamed copy
- Saves preferred naming rules locally in the browser
- Creates an optional JSON filing record

How to test on a computer
1. Open index.html in Chrome, Edge, or Safari.
2. Choose a document or image.
3. Select a category and answer the questions.
4. Review the suggested folder and filename.
5. Click “Save renamed copy.”

How to test on iPhone
The most reliable way is to host this folder on any free static host such as GitHub Pages.
When hosted, opening it in Safari lets the file picker offer the camera.
After downloading the renamed file, use the iOS Share sheet and choose Proton Drive.

Current prototype limits
- No OCR yet.
- No direct Proton Drive upload.
- It does not convert photos into PDF yet; it preserves the selected file type.
- Rules are saved only on the current browser/device.

Privacy
All processing is local in the browser. No file or answer is uploaded by this prototype.
