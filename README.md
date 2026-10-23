# The Wild Wood — Spatial Narrative Study

A compact headphone listening prototype for spatial audiobook concept, inspired by Chapter III of Kenneth Grahame's *The Wind in the Willows*.

## Try it

Open https://saragh21.github.io/3D_Audio_Book/ in a browser, use headphones, and press **Begin listening**. The 24-second sketch moves through a distant whistle, surrounding pattering, and shelter inside a hollow tree. Scene buttons jump to each state; the map can be hidden to listen without visual direction cues. Pause, restart and output controls are included. Switching tabs pauses playback.

All sound is synthesized demonstration material. There is no recorded narration, licensed SFX, finished audiobook mix or REAPER/IEM render in this package.

## The question

How can a headphone narrative communicate externalized, surrounding and approaching events? The project distinguishes intentional uncertainty from precisely localized events, and physical acoustics from narrative perspective. The full production is planned in REAPER with the IEM Plug-in Suite; HRTF choice and Ambisonic order remain open for evaluation.

## What is implemented

The browser uses Web Audio HRTF panners, per-event gain, low-pass filtering and two quiet reflection taps at 43 and 79 ms. Whistles are frequency-swept sine tones. Footsteps are short filtered-noise bursts. Event positions, timing and relative strengths use a fixed seeded score. At 16 seconds, subsequent exterior events receive additional attenuation and a 1.1 kHz low-pass cutoff to sketch enclosure. There is no head tracking, measured forest response, Ambisonic decoding, continuous source trajectory or cavity simulation.

Coordinates are listener-relative: front is negative Z, right is positive X. Panner distance attenuation is disabled because the event gain applies its own distance-dependent scaling. The visual map shows intended event positions, not measured localization or reliable perceptual distance. A master compressor controls overlap; no listener study or loudness calibration has been performed.

The full concept includes a rabbit pass-by, Rat's house and Rat's search. Those are intentionally outside this brief prototype. This is neither a complete adaptation nor a controlled experiment.

## Next production step

Replace demonstration events with separately recorded character and Foley assets, maintaining an intimate narrator distinct from scene-bound characters. Compare level-only distance rendering with combined spectral and reflection cues using identical source material and trajectories. Keep visuals hidden during listening judgements. Record externalization, apparent distance and directional uncertainty without claiming improvement before evaluation.

## Files and verification

`docs/index.html` contains the interface and short case study; `docs/style.css` contains the visual theme; `docs/app.js` contains the deterministic event score and audio renderer. JavaScript syntax checks passed. Browser layout and audio playback remain unverified because the development preview service was unavailable. Test on desktop and mobile headphones before presenting it as a finished portfolio release.
