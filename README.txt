FileNest — Scanner Upgrade

New: Batch mode, faster auto-capture, meaningful framing guide, Original/Document/B&W review modes, optional FileNest watermark (OFF by default), multipage PDF, JPEG batch export, and a slightly tighter crop to reduce table/background slivers.

Auto capture now requires 4 stable frames rather than 6 and tolerates normal hand movement.

Document enhancement is non-generative: it adjusts brightness/contrast only and does not invent or replace document content.


BALANCED AUTO-CAPTURE UPDATE
----------------------------
- Auto-capture now requires about 0.9 seconds of a good four-corner lock.
- Four stability bars remain, but they are confidence indicators rather than an instant trigger.
- Normal hand movement is tolerated up to a higher movement threshold.
- A brief wobble lowers confidence instead of resetting immediately.
- The lock resets only after roughly 0.42 seconds without a good detection.
- Corner positions are smoothed more conservatively before capture.
- A brief 90 ms settling delay is added after lock before the final frame is captured.

Batch mode, PDF/JPEG output, enhancement modes, watermark, and no-sidecar behavior are unchanged.


STRICT CORNER LOCK UPDATE
-------------------------
This update fixes false/early auto-capture.

Auto-capture now requires ALL of the following:
- A valid four-corner document quadrilateral.
- The quadrilateral must be convex and sufficiently rectangular.
- The page must occupy a reasonable portion of the camera frame.
- Opposite sides must be reasonably consistent.
- All four corners must be inside the camera frame.
- A green four-corner outline must actually be visible.
- Six consecutive good corner confirmations.
- Approximately 1.4 seconds of maintained lock after the corners are established.

If FileNest sees only a questionable contour, it displays:
"Finding the four page corners…"
and automatic capture is blocked.

Batch mode, PDF/JPEG output, enhancements, watermarking, and no-sidecar behavior
are unchanged.


CAMERA SAFE BATCH BUILD
-----------------------
This build intentionally starts from the last known camera-working version.

Included:
- Review after every batch page.
- Retake / Next Page / Finish Batch & Continue.
- Explicit camera error diagnostics shown in red inside the scanner.
- Stale camera streams are stopped before reopening.
- Existing strict four-corner lock remains unchanged.

Temporarily NOT included:
- The experimental light-background fallback detector.

The page displays "Build: Camera Safe Batch" under the FileNest heading so you
can verify that Safari/GitHub Pages is actually serving this build rather than a cached older one.
