FileNest v4.6 — Security Update
Updated: 19 Aug 2026

SECURITY CHANGES
- Personal names are removed from public index.html.
- Exact Proton Drive folder paths are removed from public index.html.
- The private filing map is imported locally and stored only in that browser.
- A Content Security Policy blocks outbound network connections.
- No Proton password, token, session key, or credential is stored.

SETUP
1. Upload only the files in FileNest_v4_6_SECURITY_PUBLIC.zip to GitHub.
2. NEVER upload FileNest_PRIVATE_CONFIG_DO_NOT_UPLOAD.json to GitHub.
3. On your phone, open FileNest.
4. Under Private filing map, choose Import private filing map.
5. Select FileNest_PRIVATE_CONFIG_DO_NOT_UPLOAD.json.
6. FileNest reloads and uses your filing structure locally.

If browser/site data is cleared, import the private configuration again.

UNCHANGED
- Still-camera scanning
- Batch mode
- Frozen corner editor
- PDF/JPEG
- Watermark behavior
- Share Sheet saving
