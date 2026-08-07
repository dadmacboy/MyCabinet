FileNest v3 — Proton Structure Edition
======================================

WHAT CHANGED
- Replaced the old generic filing paths with the finalized numbered Proton Drive structure.
- Added routing for:
  01 Personal & Family
  02 Military & Veteran
  03 Medical
  04 Financial
  05 Employment & Career
  06 Education
  07 Home & Property
  08 Vehicles
  09 Immigration & Travel
  10 Receipts
  11 Reference Library
  12 Technology & Apps
  99 Inbox
- Added subtype-aware routing. Examples:
  - W-2 -> 04 Financial/Taxes/{Tax Year}
  - VA DBQ -> 02 Military & Veteran/VA/Disability/DBQs
  - VA decision -> 02 Military & Veteran/VA/Disability/Decisions
  - DD214/discharge -> 02 Military & Veteran/Military Records/Separation
  - Security clearance -> 02 Military & Veteran/Military Records/Security Clearance
  - Passport/citizenship -> 09 Immigration & Travel/Passports & Citizenship
  - Travel authorization -> 09 Immigration & Travel/Travel Authorizations
  - Receipt -> 10 Receipts/{Purchase|Service|Subscription|Other}
  - Angelus/reference media -> 11 Reference Library/Catholic/Angelus
  - Unknown/unsure -> 99 Inbox
- Saved filing rules now use a new v3 browser-storage key, so older prototype rules will not override the new structure.
- Existing scanner, perspective correction, manual/auto capture, Share Sheet, download, and filing-record features are preserved.

CURRENT BEHAVIOR
1. Scan or choose a document.
2. Choose the closest document category.
3. Complete the short context fields.
4. FileNest produces a filename and an exact suggested Proton Drive path.
5. Review/edit if needed.
6. Share to Proton Drive, Google Drive, Files, or another app.

SAFE FALLBACK
If a document does not fit a known route, FileNest recommends:
  /99 Inbox/
This prevents uncertain documents from being filed into the wrong permanent folder.

IPHONE CAMERA REQUIREMENT
The browser camera API requires an HTTPS page in Safari/Chrome.
Host FileNest_v3.html on GitHub Pages or another HTTPS static host for camera scanning.

LIMITATIONS STILL PRESENT
- No OCR or automatic document recognition yet.
- Scans are one-page corrected JPEGs, not multi-page PDFs.
- FileNest cannot directly create/navigate Proton Drive folders through the browser; Proton Drive is selected through the iOS Share Sheet.
- Vehicle-specific subfolders may need to be created the first time they are used.

RECOMMENDED V3 TEST CASES
- 2026 W-2
- VA rating/decision letter
- VA DBQ
- Medical imaging or visit summary
- Resume
- Passport/citizenship record
- Travel authorization
- Vehicle maintenance receipt
- Unknown document (confirm it routes to 99 Inbox)

NEXT DEVELOPMENT STEP
After routing tests pass, add local OCR/document recognition so FileNest can suggest the category and fields automatically while keeping processing private/on-device where possible.


IPHONE / HOME SCREEN ICON
- The package now includes the FileNest folder-in-a-nest icon with the wordmark removed.
- apple-touch-icon.png is the 180x180 iPhone Home Screen icon.
- filenest-icon-1024.png is the high-resolution source for use in Apple Shortcuts or other launchers.
- The HTML now references the Apple touch icon and web-app manifest automatically.
- If you host this folder on HTTPS and use Safari > Share > Add to Home Screen, iPhone should use the FileNest icon.
