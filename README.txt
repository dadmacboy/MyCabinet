FileNest — PDF Creation Fix
============================

This build keeps the working native scanner unchanged.

PDF FIX
- Replaced the previous mixed-chunk PDF generator with a contiguous Uint8Array build.
- This is more reliable in mobile Safari.
- PDF creation now validates that the generated Blob and File are non-empty.
- The Review Scan screen stays open if PDF creation fails.
- Any PDF error is shown directly on the review screen instead of silently closing.
- JPEG behavior is unchanged.

TEST
1. Scan a document.
2. Leave PDF selected.
3. Tap Use Scan & Continue.
4. You should see "Creating PDF…" briefly.
5. Then FileNest should show "PDF scan ready to file" and move to Step 2.
