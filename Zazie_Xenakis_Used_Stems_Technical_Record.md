# Technical provenance record — Xenakis International Competition composition

**Artist:** Zazie Productions  
**Record date:** 6 November 2026  
**Status:** Both source stems incorporated into the current composition and subsequently altered by the artist. The nature and values of those subsequent changes are not yet documented.  
**Original audio source:** `Xenakis Internation Contest Demo.m4a` (user-supplied)  
**Stem format:** 24-bit PCM WAV, stereo, 24,000 Hz; 212.948 seconds; aligned at 00:00.  
**Important distinction:** Parameters below describe the *original generated stems*, not necessarily the processed stems or the finished composition. These are original Xenakis-inspired algorithms, not reproductions of Xenakis's GENDYN program.

## Shared source-energy analysis

The original recording was downmixed and decoded to mono for analysis. The root-mean-square (RMS) amplitude was measured in successive 100 ms frames, smoothed using a Gaussian filter with standard deviation of three frames, and normalized to the 10th and 93rd percentile of frame RMS for stem 05, or the 10th and 94th percentile for stem 08. The normalized result was clipped to [0,1] and linearly interpolated in time. Call this envelope E(t).

For analysis frames x_k of length M:

`RMS_k = sqrt((1/M) * sum_{n=0}^{M-1} x_k[n]^2)`

`E(t) = clip((smooth(RMS)(t) - Q_10)/(Q_hi - Q_10), 0, 1)`

Here `Q_hi = Q_93` for 05, `Q_94` for 08. The shared source-energy concept does not imply the two stems have identical envelope normalizations.

## 05 — Source-Derived Granular Cloud

**Status:** Used in composition; artist-modified after generation.  
**Technique:** Source-derived probabilistic granular resynthesis with energy-following event density.  
**Generation seed:** `194812`  
**Generated grain count:** 1,295  
**Grain duration:** Uniformly selected from 18–105 ms.  
**Playback speed:** Uniformly selected from 0.65–1.70 times source rate.  
**Onset process:** Inhomogeneous Poisson-style event scheduling using exponential waiting times, with instantaneous rate:

`lambda_05(t) = 2 + 14 E_05(t)` events/second.

`Delta t ~ Exponential(mean = 1/lambda_05(t))`.

**Extraction:** Each grain samples the source recording near the corresponding timeline position, with a normally distributed offset of standard deviation 0.7 s, and applies a Hann window. Playback speed varies independently by grain. Grain stereo position is independently sampled uniformly across the pan range [-1,+1] and mapped using equal-power panning.  
**Signal construction:** For a grain of N samples, source position p and playback-rate factor r:

`g[n] = x[p + r*n] * Hann_N[n]`, with interpolation and valid-source-index clipping.

**Artistic role:** Fragments of the original liquid, brittle, and mechanical sound palette are redistributed as a microscopic stochastic cloud, retaining material continuity with the source composition.

## 08 — Brownian Liquid Drift

**Status:** Used in composition; artist-modified after generation.  
**Technique:** Bounded Gaussian random walks governing correlated grain playback speed and stereo placement.  
**Generation seed:** `20261106`  
**Generated grain count:** 608  
**Grain duration:** Uniformly selected from 35–150 ms.  
**Onset rate:**

`lambda_08(t) = 0.7 + 7 E_08(t)` events/second.

`Delta t ~ Exponential(mean = 1/lambda_08(t))`.

**Pan walk:** Initial pan 0; on each grain:

`p_(k+1) = clip(p_k + epsilon_k, -0.95, +0.95)`

`epsilon_k ~ Normal(0, 0.16^2)`.

**Playback-rate walk:** Initial rate 1.0:

`r_(k+1) = clip(r_k + eta_k, 0.55, 1.70)`

`eta_k ~ Normal(0, 0.065^2)`.

**Extraction:** Hann-windowed grains drawn near the source timeline position with Gaussian source-offset standard deviation 0.35 s. Each grain inherits the current correlated playback rate and pan value. Equal-power panning places it in stereo.  
**Artistic role:** A liquid texture whose spectral speed and spatial position drift with statistical continuity; unlike independent randomization, successive grains retain local memory.

## Comparative compositional significance

05 organizes **where and when** short fragments of the original recording reappear, using energy-dependent event rates and independent grain-level transformations. 08 organizes **how their behavior changes from one event to the next**, using bounded, correlated random walks. Their combination creates a relationship between statistical populations of sound events and the continuous local evolution of those events.

## Authorship, credit, and disclosure

Original source recording and final artistic arrangement: **Zazie Productions**. Algorithmic companion stems generated for the artist with ChatGPT-assisted Python synthesis. Subsequent editing, layering, processing, and placement by the artist; exact changes have not yet been supplied. The stems are **Xenakis-inspired** and should not be described as literal implementations of his historical GENDYN code. No ISRC, ISWC, IPI, publisher identifier, or final track title is assumed or assigned in this record.

## To complete the final-work record

For each stem, note: regions used, start/end timestamps, gain and automation, time-stretch or pitch-shift, filtering, effects and plugin settings, reversals, edits, layering, bounce/render settings, and whether the processed result remains recognizably source-derived. These fields remain **unverified**, not blank by oversight.
