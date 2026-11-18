[![DOI](https://img.shields.io/badge/DOI-10.82901%2Fnemar.on007714-blue)](https://doi.org/10.82901/nemar.on007714)

<!-- nemar:provenance -->
## Provenance

This dataset is mirrored on NEMAR from OpenNeuro.

- Source: [ds007714](https://openneuro.org/datasets/ds007714)
- DOI: [10.18112/openneuro.ds007714.v1.0.0](https://doi.org/10.18112/openneuro.ds007714.v1.0.0)

## Contributed notes (version 1.0.1)

- The SNIRF files do not open in MNE-Python 1.13: read_raw_snirf stops with "The time unit None is not supported by MNE" (checked on sub-s08 and sub-s61). The files need regenerating with SNIRF v1.1 TimeUnit, LengthUnit and dataUnit; this version changes no SNIRF file.
- sub-s45/nirs/sub-s45_task-visual_nirs.snirf is truncated in OpenNeuro ds007714 1.0.0: the published file holds 7,771,051 bytes, while its HDF5 superblock gives an end-of-file address of 14,432,504 bytes, so HDF5 readers report a truncated file.
- The sidecars of sub-s45 (whose SNIRF file is truncated) are left as published: its channels.tsv keeps the published channel names and its coordsystem.json has no NIRSCoordinateSystemDescription, so sub-s45 uses a different channel naming style from the other 63 subjects.
- 42 of the 64 events.tsv files are not sorted by onset (BIDS validator warning EVENT_ONSET_ORDER).
- participants.tsv lists 11 participants with no subject folder: sub-s03, sub-s07, sub-s39, sub-s46, sub-s49, sub-s56, sub-s64, sub-s72, sub-s73, sub-s74 and sub-s77 (all their values are n/a).
- dataset_description.json still holds template text. The OpenNeuro record doi:10.18112/openneuro.ds007714.v1.0.0 lists the creators Gemma Bale, John O'Brien and Emilia Butters; cite that record.
