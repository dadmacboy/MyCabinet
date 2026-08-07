FileNest — PDF/JPEG Scan Output Update
=========================================

This build preserves the working native scanner and does NOT change the
document-corner detection algorithm.

NEW SCAN OUTPUT FLOW
1. Scan / auto-capture the document.
2. Review the perspective-corrected scan.
3. Choose:
   - PDF — Document (default)
   - JPEG — Image
4. Tap Use Scan.
5. FileNest continues to classification, naming, and filing.

PDF
- Default for scanned documents.
- Creates a real single-page PDF containing the corrected scan.
- Recommended for records, receipts, official documents, and archives.

JPEG
- Creates a .jpg image.
- Useful when a website does not accept PDF and requires a picture.

NO EXTRA TEXT FILE
- The iOS Share Sheet payload now shares ONLY the document file.
- The previous "Suggested folder" text was removed from the share payload
  because iOS/receiving apps can treat shared text as an additional text item.
- Scanning itself does not create any .txt file.
- "Export filing record (JSON)" remains an optional manual button. It only
  creates a JSON record when you deliberately tap it.

IMPORTANT
- Upload all files in this ZIP to the GitHub repository root.
- Replace the current index.html.
- The scanner detector itself is unchanged from the working Native Scanner build.
