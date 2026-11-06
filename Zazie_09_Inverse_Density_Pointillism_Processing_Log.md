# Zazie Productions — Xenakis Competition: Processing / Provenance Log

**Recorded:** 6 November 2026  
**Logic project:** Xenakis Internation Contest.logicx (visible in screenshots)  
**Region/track described by composer:** `09_Inverse_Density_Pointillism_2`  
**Processed demonstration:** `09_Inverse_Density_Pointillism Stride Fragmenter.m4a`  
**Processing:** Freakshow Industries Backmask, used within Stride FX (as visible in the Stride FX device rack), with variations over time. The demonstration is more compressed than the intended final mix; it must not be treated as final-master loudness or dynamics.

## Original generative method — stem 09

Inverse-energy stochastic pointillism. Events were scheduled using a time-varying Poisson process whose intensity was **greater in quieter portions of the original source recording**:

\[\lambda(t) = 0.45 + 2.4[1-E(t)] \quad \text{events/second}\]

Here \(E(t)\in[0,1]\) was the normalized, smoothed RMS energy of the source demo. Conditional interarrival time at current time was drawn approximately as \(\Delta t\sim\mathrm{Exponential}(1/\lambda(t))\). This was an event-by-event local-rate approximation, not an exact inversion of the integrated time-varying intensity.

Original stem: **456 events**; resonant frequencies selected from **223, 307, 419, 557, 739, 997 Hz**, with log-frequency Gaussian perturbation \(f=f_0 2^{\epsilon}\), \(\epsilon\sim N(0,0.045^2)\). Event durations were **100–550 ms**. Each event was a damped, lightly frequency-modulated sinusoid, with approximately 50% of events also incorporating a grain from the source demo. Original generation seed **20261106**. Original generated audio was stereo 24-bit PCM WAV at **24 kHz**, approximately **212.948 seconds**.

## Subsequent composer-directed transformations

The composer placed a variant of this stem in Logic Pro and processed it with **Freakshow Industries Backmask and Stride FX**, including variations in settings during playback. Screenshots show a Stride FX window titled `06_Markov_Texture_Mutations_2` (different from the composer's identification of the processed audio as stem 09), so the exact track routing of these screenshots is **not independently verified**. This discrepancy should be reconciled from the saved Logic project before final submission documentation.

**Visible Stride FX state:** Backmask appears in the device rack; Stride FX is in a mapped modulation view. Visible motion includes **Bloom** and a synced **1/8** rate. Playback panel shows tempo sync and 120 BPM. Backmask macro controls include Max Size, Mix, Size, Stuck, Time Align, Trigger Mode and Trigger Type. At least two snapshots have different values, demonstrating settings variation, but screenshots alone do not establish whether changes were automated, manually performed, or captured at different saved states.

**Approximate values visible across the screenshots** (screen-reading, not plugin-state export):

| Control | Screenshot A | Screenshot B |
|---|---:|---:|
| Max Size | 29% | 65% |
| Mix | 99% | 27% |
| Size | OFF | OFF |
| Stuck | 53% | 19% |
| Time Align | 93% | 81% |
| Trigger Mode | OFF | OFF |
| Trigger Type | 68% | 19% |

The earlier screenshot shows Backmask's own interface in the foreground and a different set of apparent macro values behind it; do not treat these as a complete parameter history.

## Audio demonstration

The provided `.m4a` is **174.763 seconds**, **AAC stereo at 48 kHz** (container metadata). It is a processed excerpt/export, not the original 212.948-second generative WAV. Per composer, the demonstration's compression is not representative of the final mix. The audible excerpt has rounded, pitch-bending electronic chirps, bubbles, and short sequences interspersed with silence; no claim is made about a measured dynamic-range change without comparing matched exports.

## Proposed submission-ready description (provisional)

> A pointillistic stochastic layer was generated using an inverse-energy event-density function, increasing the probability of resonant events during relatively sparse passages of the source composition. Its initial frequency collection and event durations were probabilistically varied, with selected events incorporating fragments of the source recording. The composer subsequently transformed a variant of this material through Freakshow Industries Backmask and Stride FX, introducing time-dependent fragmentation and timbral variation. The processed example is not representative of the final mix's compression or dynamic treatment.

## Provenance / limitations

- Artist/composer: **Zazie Productions**.
- Original mathematical generation: custom Python-based stochastic synthesis for this project; not a reconstruction of a Xenakis work.
- Subsequent editing, selection, processing and integration: composer.
- This note records the **original source algorithm** and **visible subsequent effects**, not the complete final render signal chain.
- No ISRC, ISWC, IPI or registration identifiers have been assumed.
- Composer previously reported using and modifying stems `05_Source_Derived_Granular_Cloud` and `08_Brownian_Liquid_Drift` as well; this is an additional entry, not a replacement for those records.
