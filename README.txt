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
