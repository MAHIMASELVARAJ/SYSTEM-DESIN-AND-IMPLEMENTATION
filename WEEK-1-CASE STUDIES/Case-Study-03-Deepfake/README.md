**Case Study 3 — Catching a Deepfake Voice Mid-Call at [Illustrative: "Kestrel Enterprise Communications"]**

**Executive Summary**

A company providing cloud-based video and voice conferencing for enterprise clients faces
rising incidents of deepfake voice and video fraud during live calls — including
impersonation of executives to authorize fraudulent payments. This case study proposes a
detection gateway built directly into the live media pipeline that flags or blocks synthetic
audio/video in real time, during the call itself, rather than analyzing recordings afterward.

**The Problem Statement**

AI-generated voice cloning and face-swapping tools have become good enough to convincingly
impersonate a real person on a live call. Attackers have used this to trick employees into
transferring money or sharing sensitive information, believing they are speaking to a
trusted executive or colleague. Existing deepfake detection tools mostly analyze video or
audio clips after the fact — useful for forensic investigation, but too late to prevent
damage during a live, time-sensitive call where a decision (like a wire transfer approval)
might be made in the moment.

**The Solution**

A detection component embedded directly inside the cloud media pipeline that already routes
enterprise video/voice calls. As audio and video streams flow through the existing
infrastructure, the system analyzes them in real time for signals characteristic of
synthetic generation (voice cloning artifacts, unnatural facial micro-movements, audio-visual
sync mismatches), scores the likelihood the stream is synthetic, and — above a set
confidence threshold — intervenes on the live call: muting, flagging visibly to participants,
or blocking the stream outright.

**The Implementation**

Integrate a stream interceptor into the existing cloud media gateway (SFU) architecture, with minimal added latency.

Build real-time audio and video analysis models that run on short rolling windows of the stream rather than full recordings.

Combine audio and video signals into a single confidence score per active call segment.

Set policy thresholds for Allow / Flag (visible warning to participants) / Block.

Wire the Block/Flag decision into the media gateway's stream control so the intervention happens live, not after the call ends.

Store flagged segments securely for post-incident review and evidence.

**Results (Target outcomes to validate during prototyping)**

Target: detection latency low enough to intervene within the first few seconds of a synthetic segment appearing (specific target, e.g. under 3 seconds, to be set through testing).

Target: acceptable false-positive rate on flagging real participants as synthetic — needs careful tuning and testing with diverse real speakers/lighting conditions.

Target: measurable reduction in successful "voice clone fraud" scenarios in red-team simulated attack testing, compared to a baseline with no real-time detection.

**Conclusion / Takeaway**

Detecting deepfakes after a call is over doesn't stop the fraud that happens during the call.
Moving detection into the live media pipeline itself, with the ability to actually intervene
on the stream in real time, is what turns this from a forensic tool into a genuine
protective one — and it's the part worth prototyping carefully, including realistic testing
against false positives.
