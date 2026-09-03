# Vinyl Playback Fingerprint

## A Persistent Multidimensional Method for the Objective Characterisation and Comparison of Analogue Record Playback

**Michelangelo Canonico**  
Direct Sound Records · DSR Technical Journal  
**DSR-VPF v1.0 · VPF-Core-1K v1.0**  
Published 3 September 2026  
DOI: https://doi.org/10.5281/zenodo.22287619  
Licence: CC BY 4.0

## Abstract

Objective analysis of vinyl playback commonly reports speed error, wow and flutter, channel balance, crosstalk, distortion, harmonic content and noise as separate results. Those measurements are useful, but their isolation makes it difficult to preserve the technical identity of a measurement session, determine whether a later session is meaningfully different, or compare records, pressings and playback systems without losing context.

This paper defines the DSR Vinyl Playback Fingerprint Method (DSR-VPF) v1.0: a persistent, versioned, multidimensional measurement object that combines heterogeneous objective results with validity state, repeatability or uncertainty information, acquisition provenance and comparison rules.

The Fingerprint is not the radar graph used to display it; the graph is one projection of an underlying machine-readable object. The first fixed profile, VPF-Core-1K v1.0, comprises speed accuracy, weighted wow and flutter, channel balance, stereo separation, directional crosstalk asymmetry and total harmonic distortion.

## Core contribution

A DSR-VPF Fingerprint is formally treated as a persistent object rather than a transient chart:

```text
F = (id, x, z, q, u, p, v)
```

where the object retains identity, raw measurements, normalised projection coordinates, quality/admissibility states, uncertainty or repeatability information, provenance and method/profile/projection versions.

The graphical representation is therefore a projection of the Fingerprint, not the Fingerprint itself.

## VPF-Core-1K v1.0

The first fixed profile contains six ordered dimensions:

1. **Speed accuracy** — absolute playback-speed error.
2. **Weighted wow and flutter** — weighted rotational instability with the measurement convention explicitly named.
3. **Channel balance** — absolute left/right level difference.
4. **Stereo separation deficiency** — departure from the profile reference separation.
5. **Directional crosstalk asymmetry** — difference between the two directional separation measurements.
6. **Total harmonic distortion** — qualified THD result under a declared analysis method.

The machine-readable profile in `specification/vpf-core-1k-v1.0.json` fixes dimension order, diagnostic transforms, weights and comparison coverage.

Display bounds are stable graphical coordinates. They are **not** pass/fail tolerances, audibility thresholds or universal sound-quality criteria.

## Data-quality states

Every dimension carries an explicit evidence state:

- `primary_valid`
- `supporting_valid`
- `diagnostic_only`
- `variable_or_unreliable`
- `unavailable`

Invalid or missing data must not be silently plotted as zero. A missing measurement and a perfect measurement are not equivalent.

The v1.0 quality-to-comparison weighting is:

```text
primary_valid          1.0
supporting_valid       0.5
diagnostic_only        0.0
variable_or_unreliable 0.0
unavailable            0.0
```

## Comparison classes

DSR-VPF defines four comparison classes:

- **Class A — Longitudinal:** same record and playback system measured over time or before/after an intervention.
- **Class B — Playback-system:** controlled comparison in which a playback variable is deliberately changed.
- **Class C — Record/pressing:** records, copies, pressings or production stages compared through a qualified reference chain.
- **Class D — Descriptive only:** sessions may be displayed together but are not eligible for an aggregate numerical distance.

Compatibility is assessed before distance. Numerical comparison requires at least two-thirds aggregate profile coverage under VPF-Core-1K v1.0.

## Distance and coverage

For compatible fingerprints, DSR-VPF uses a missing-data-aware weighted Euclidean distance in normalised profile space. The result must be accompanied by a separate coverage value so a distance calculated from an incomplete set of valid dimensions cannot be mistaken for a complete comparison.

Neither distance nor radar-polygon area is a universal sound-quality score.

## Vinyl Playback Fingerprint versus Record Fingerprint

A normal vinyl measurement contains contributions from the record, stylus, cartridge, tonearm, turntable, phono stage, capture chain and environment. The general term is therefore **Vinyl Playback Fingerprint**.

The narrower term **Record Fingerprint** should be reserved for measurements made through a declared and qualified reference chain whose relevant variables and repeatability are controlled sufficiently for record/pressing comparison.

## Reference implementation

**Groove Scope** is designated as the first reference implementation of DSR-VPF.

Public measurement archive: https://github.com/directsoundrecords/groove-scope-measurements

## Priority statement

To the author's knowledge, the DSR Vinyl Playback Fingerprint Method is the first publicly documented method to transform multiple heterogeneous objective vinyl-playback measurements into a persistent, versioned, multidimensional graphical fingerprint specifically designed for comparison between documented sessions.

This is deliberately a bounded public-documentation statement. It does not claim invention of the underlying vinyl measurements, graphical plots, conventional audio fingerprinting or automated pressing-quality control, and it is not a patentability or freedom-to-operate opinion.

See `metadata/prior_art_search_note.md` for the search scope and limitations.

## Validation status

DSR-VPF v1.0 fixes the method architecture and initial profile. Empirical repeatability, reproducibility, inter-device agreement and controlled-intervention validation remain ongoing and should be reported separately rather than silently altering the v1.0 definition.

## Canonical publication

The complete DOI-bearing publication, bibliography, figures, equations, appendices and archival package are preserved at:

https://doi.org/10.5281/zenodo.22287619

Human-readable DSR Technical Journal edition:

https://directsoundrecords.com/vinyl-playback-fingerprint/

## Suggested citation

Canonico, M. (2026). *Vinyl Playback Fingerprint: A Persistent Multidimensional Method for the Objective Characterisation and Comparison of Analogue Record Playback* (Version 1.0). DSR Technical Journal. Direct Sound Records. https://doi.org/10.5281/zenodo.22287619
