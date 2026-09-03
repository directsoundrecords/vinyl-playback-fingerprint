# DSR Vinyl Playback Fingerprint Method (DSR-VPF)

**Open specification and reference materials for a persistent, versioned, multidimensional method for objective comparison of analogue record playback.**

**Method:** DSR Vinyl Playback Fingerprint Method (DSR-VPF) v1.0  
**Core profile:** VPF-Core-1K v1.0  
**Author:** Michelangelo Canonico  
**Publisher:** Direct Sound Records  
**Published:** 3 September 2026  
**DOI:** [10.5281/zenodo.22287619](https://doi.org/10.5281/zenodo.22287619)  
**Licence:** CC BY 4.0

## What is a Vinyl Playback Fingerprint?

Objective vinyl analysis commonly reports speed error, wow and flutter, channel balance, crosstalk, distortion, harmonic content and noise as separate results. DSR-VPF treats heterogeneous objective measurements as one persistent measurement object that can be stored, versioned and compared between documented sessions.

The Fingerprint is **not** the radar graph used to display it. The graph is one projection of an underlying machine-readable object containing raw values, normalised coordinates, quality/admissibility states, provenance and version information.

The first fixed profile, **VPF-Core-1K v1.0**, comprises:

- speed accuracy;
- weighted wow and flutter;
- channel balance;
- stereo separation;
- directional crosstalk asymmetry;
- total harmonic distortion.

## Priority statement

To the author's knowledge, the DSR Vinyl Playback Fingerprint Method is the first publicly documented method to transform multiple heterogeneous objective vinyl-playback measurements into a persistent, versioned, multidimensional graphical fingerprint specifically designed for comparison between documented sessions.

This is a bounded public-documentation claim, not a patentability or freedom-to-operate opinion. DSR-VPF does not claim invention of the underlying vinyl measurements, radar charts, audio identification, or conventional record-quality control.

## Reference implementation

**Groove Scope** is designated as the first reference implementation of DSR-VPF.

Public Groove Scope measurement archive:  
https://github.com/directsoundrecords/groove-scope-measurements

## Canonical publication

**Vinyl Playback Fingerprint: A Persistent Multidimensional Method for the Objective Characterisation and Comparison of Analogue Record Playback**

Permanent scholarly record:  
https://doi.org/10.5281/zenodo.22287619

DSR Technical Journal:  
https://directsoundrecords.com/vinyl-playback-fingerprint/

## Repository structure

```text
paper/
  DSR_Vinyl_Playback_Fingerprint_Method_v1.0.md

specification/
  dsr-vpf.schema.json
  vpf-profile.schema.json
  vpf-core-1k-v1.0.json
  example-fingerprint-v1.0.json

metadata/
  citation.bib
  prior_art_search_note.md

CITATION.cff
LICENSE.txt
CHANGELOG.md
```

The DOI-bearing PDF and complete archival package are preserved in Zenodo under the DOI above.

## Citation

Canonico, M. (2026). *Vinyl Playback Fingerprint: A Persistent Multidimensional Method for the Objective Characterisation and Comparison of Analogue Record Playback* (Version 1.0). DSR Technical Journal. Direct Sound Records. https://doi.org/10.5281/zenodo.22287619

## Licence

© 2026 Michelangelo Canonico. Except where otherwise noted, the documentation, method specification and associated materials in this repository are licensed under the **Creative Commons Attribution 4.0 International (CC BY 4.0)** licence.
