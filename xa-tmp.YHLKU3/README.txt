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


CAMERA PERMISSION FIX
---------------------
The Scan Document button now calls navigator.mediaDevices.getUserMedia()
immediately from the user's tap.

Why:
- iPhone Safari requires the website to request camera access.
- A website cannot silently grant its own camera permission.
- Safari should prompt the user the first time the site requests camera access.
- If permission was already allowed, the camera opens without prompting again.

Recovery:
- FileNest now shows an Enable Camera button when access is blocked or fails.
- If Safari has remembered "Deny", Safari may not display the prompt again.
  In that case, change the website Camera permission to Allow in Safari/site settings,
  then return to FileNest and tap Enable Camera.

The document detector, PDF/JPEG output, and no-sidecar behavior are otherwise unchanged.
