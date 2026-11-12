# Xenakis competition · Logic Pro project audit

**Project** — Xenakis Internation Contest.logicx  
**Audited** — November 12, 2026  
**Current mix** — 6:04.497, fixed-media stereo

## Render and delivery

| File | Format | Duration | Integrated loudness | Loudness range | True peak |
|---|---|---:|---:|---:|---:|
| Xenakis-High-Resolution-Master-48k32f.wav | Stereo PCM, 48 kHz, 32-bit float | 6:04.497 | −20.2 LUFS | 15.2 LU | −1.1 dBTP |
| Xenakis-Current-Mix-44k1-24bit.wav | Stereo PCM, 44.1 kHz, 24-bit | 6:04.497 | −20.2 LUFS | 15.2 LU | −1.1 dBTP |

Logic bounced the existing Stereo Out across bars 1 through 183, with automation and effects rendered, **Include Audio Tail** enabled, and normalization off. The 48 kHz master uses the project’s native sample rate. The original 24-bit test hit full scale. The floating-point render captured 14 over-range channel samples, with its highest peak around 2:43.112. Both delivered files use the same floating-point pass and a single **−1.5 dB** gain adjustment. The 44.1 kHz copy was resampled and dithered to 24-bit. Neither deliverable received any new compression, limiting, EQ, or arrangement edits. The two Logic test passes differed at the waveform level, so sample-for-sample equivalence to a separate playback pass was not established. Quality control used file decoding, sample-peak and true-peak measurement, and an end-of-file check. The rendered range includes about 0.497 seconds after bar 183.

**Competition status** — The published call specifies **7–15 minutes** and a stereo WAV or AIFF at **44.1 kHz, 16 or 24 bit**. The 44.1 kHz file meets the encoding specification. This version needs **55.503 seconds of additional duration** to reach 7:00. The bounces preserve the current form. [Published call](https://musiquecontemporaine.org/aides-concours-appels/6th-international-competition-electronic-music-iannis-xenakis) · [Organizer’s rules page](https://xenakis.web.auth.gr/rules/)

## What the project supports

### A fixed grid with off-grid attacks

Logic’s tempo list shows one event at **120 BPM**. The MIDI file confirms one **4/4** meter event, one tempo event and a C-major project key signature. At this tempo, one bar is **2 seconds**, one quarter note is **500 ms**, and the nominal sixteenth is **125 ms**. The MIDI export contains **112 note-ons at 105 unique onset positions** across **14 MIDI regions**. All 112 onsets fall off the exact straight-sixteenth grid at the exported **480 PPQ** resolution. This measures displacement from the grid. It does not identify the source of that displacement or establish stochastic timing.

The MIDI events cover **all 12 pitch classes**, span MIDI notes **29–100**, and use velocities **1–102**. Patch transpositions, samples, and atonal or noisy timbres can differ from the MIDI key values. The C-major setting is a project signature, not a finding about the work’s harmonic language.

### Shared attacks, uneven returns, and density

- **Cave Insects and Circuit Monks** share five identical onset/pitch/velocity triples. Every Circuit Monks note-on has a match in the late Cave Insects region, at approximately **4:22.020, 4:23.883, 4:30.556, 4:30.599, and 4:32.148**. That is a concrete example of two patches articulating the same attack pattern, including a pair of events about **43 ms** apart.
- **Sheets Of Metal** contains **51 note-ons** across four regions. Region entries fall at **0:50, 2:44, 3:32, and 4:02**, giving gaps of **114, 48, and 30 seconds**. The successive regions contain **6, 23, 3, and 19** note-ons. These unequal gaps and event counts describe the actual placement of recurring material.
- **Bowed waterphone** material labeled approximately A♯6 returns in two **22-second regions** at **4:16** and **4:46**. The corresponding source files have equal frame counts and a measured left-channel correlation of **1.000** across their full source duration. The region-entry displacement is **30 seconds**.
- **Region density** reaches **12 simultaneous regions** in the arrangement inventory during **0:18–0:20** and **0:26–0:28**. This is an overlap count of the displayed audio and MIDI regions. Patch voices, reverb tails and audible loudness are separate quantities.
- **Dead Air Apparatus** begins at **0:00** and returns at **5:38–5:52**. That return overlaps the first **10 seconds** of the closing descending-tone region at **5:42–6:04**.

### Algorithm-labeled source layers

Four files each contain **212.948 seconds** of 48 kHz, 24-bit stereo audio. The arrangement deploys excerpts of different lengths. The asset names and placements support the following description of the materials. The precise algorithms need source-generation code, settings, or contemporaneous notes.

| Region label | Placement | Evidence and limit |
|---|---:|---|
| 05_Source_Derived_Granular_Cloud | 0:06–1:02 | Early texture labeled as source-derived granular audio. Grain size, window, overlap and trigger distribution are unverified. |
| 08_Brownian_Liquid_Drift | ~0:02.30–2:38.99 | Long early audio layer. The name identifies a Brownian reference. A random-walk process, its step distribution and the parameter it controls are unverified. |
| 09_Inverse_Density_Pointillism_2 | 1:28–~3:28.02 | Mid-form excerpt. The name identifies pointillism and inverse density. The variable, inverse relationship and event rule are unverified. |
| 06 - Markov Texture Mutations | 3:28–4:00 | Audio region on **Bass Metals**. A track elsewhere carries a Markov name but contains the pointillism region. The rendered Markov-named file establishes placement. Its states, order and transition matrix are unverified. |

The pointillism and Markov-named regions meet within roughly **20 ms** at **3:28**. That handoff is a stronger statement about form than a generalized claim that the entire arrangement is stochastic.

### Closing pitch motion and stereo movement

**Dark Shepard Tone 2** occupies the final **22 seconds** of the main timeline. One-second FFT windows of the source show descending spectral components, with approximate peaks near **120/180 Hz** around source second 2 and **90/145 Hz** around source second 10. Around source second 4, peaks near **57, 112, 168, 223 and 332 Hz** show several approximately integer-related components. “Descending spectral texture” is supported. The exact synthesis or an octave-crossfade Shepard/Risset construction remains unverified.

The **circuit-bent toy** source shows channel-energy changes, with one-second windows ranging from roughly **23 dB right-dominant** to windows in which the right channel is effectively silent. Its arrangement region sits at **4:04–4:36**. This supports describing substantial stereo movement in the source. Its exact in-mix trajectory depends on channel-strip pan, routing and automation.

## Arrangement inventory

Logic shows **50 numbered tracks**. The arrangement inventory includes **44 parent-level or standalone tracks** and the mixer exposes the **six instrument children** of Spectral choir repossessed. Across those parent-level and standalone lanes, the inventory contains **52 placed regions**, comprising **38 audio** and **14 MIDI**. Three standalone lanes display no region in the audited range. Counts describe timeline objects, including the choir stack’s parent MIDI region. The MIDI export also yielded 14 populated chunks.

| Tracks | Material and placement |
|---|---|
| 1–6 | Distorted miasma accent around bar 62, bowed waterphone at 45 and 59, Dead Air at 1 and 170, horror soundscape at 14, Dying Star at 26, granular cloud at 4 and descending-tone close at 172. |
| 7–12 | Damaged Artifact at 10, two regions on cheaper_impressions at 22 and 90, Sheets Of Metal at 26/83/107/122, Only Chaos at 5, waterphone sting and low-register passby at 9 and 78, pointillism at 45. |
| 13–18 | Brownian-named drift near 2, Bass Metals MIDI at 10 and Markov-named audio at 105, Wood Trees at 113 on the second Brownian-named track, Cave Insects at 3, Interdimensional Time Travel at 1 and Digital Drain Pipe at 3. |
| 19–24 | Bowed Metal Space print at 2, slippage beyond the hyperlink at 55, Interdimensional Time Travel 04 at 47, insintesi audio at 72, Alien Traveler at 54 and Spectral choir repossessed MIDI at 6. |
| 25–30 | Choir stack children **Moody Hall**, **Travelling Angels**, **Eerie Dissonance**, **Spectral Choir Phrases**, **Massive Ambient Drone** and **Reposessed**. |
| 31–36 | Exotic Metals at 25, Sizzling In The Kitchen at 10, Fractured Decay at 55, Cave Insects at 128, circuit-bent toy at 123 and bowed waterphone at 129. |
| 37–42 | Tormented Souls waterphone on the Relay Switch-named lane at 120, fast single bow at 127, Dark Fantasy ASMR at 118 and Vox-02 at 137, Circuit Monks at 132, waterphone sting on a Glass ASMR-named lane at 146, cheaper_impressions at 138. |
| 43–50 | Languid glissando at 133, Cellar Cello Waterphone at 149, bowed waterphone and HD Sound Art ASMR on track 46 at 144 and 162, Glass ASMR on 48 at 166 and Bluezone ambience on 49 near 142. Tracks 45, 47 and 50 display no region in this range. |

The Mixer shows a stereo output and the choir stack return. The automation controls shown in the arrangement were in **Read** mode. The stereo bounce captures the playback result of the automation and shared effects. The audit did not enumerate every automation node or reconstruct every plug-in’s internal modulation.

## Source credits to verify before entry

The region and file names identify several external sources. Check the source terms and any required credit for public performance, broadcast and delivery before using the competition copy. The published call describes possible concerts and broadcasts and has a condition on discographic or publication rights. This audit did not resolve any source permission. [Published call](https://musiquecontemporaine.org/aides-concours-appels/6th-international-competition-electronic-music-iannis-xenakis)

| Material | Placement | Record to check |
|---|---:|---|
| Tunetank, Horror Scary Soundscape Music | 0:26–1:33 | The ID matches Pixabay’s MP3 listing. The WAV in Logic does not change the original source encoding. [Asset](https://pixabay.com/es/music/misterio-horror-scary-soundscape-music-414108/) · [License summary](https://pixabay.com/service/license-summary/) |
| gis_sweden 437385, insintesi 787393 and monteresidencia 759431 | 0:42–2:04, 2:22–2:56.5 and 3:44–4:18 | Freesound IDs from the project filenames. Verify the individual license and attribution for each. |
| Dark Fantasy ASMR and Glass ASMR | ~3:54–4:22 and 5:30–5:48 | Project filenames carry IDs S9onYYBZJxM and 74F3klKnAfA. Confirm provenance and reuse terms. The similarly named track 41 contains a waterphone region. |
| HD Sound Art ASMR, the waterphone and sci-fi library material, and Bluezone ambience | Multiple | Match each source to the original recording or library record. Confirm the relevant terms for the rendered work. |

## Program-note draft

The piece is a fixed-media stereo work built from bowed waterphone, metallic resonances, choir-like synthesis, circuit-bent textures and rendered electronic layers. A steady editing grid holds a texture whose MIDI attacks fall between the sixteenth-note divisions. In one late passage, Cave Insects and Circuit Monks share five attacks at identical times, pitches and velocities, giving one gesture two timbres. Metal events return at progressively shorter intervals. The opening Dead Air Apparatus returns near the close and overlaps a descending spectral texture.
