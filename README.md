# AutoWarranty Vehicle-Year Evidence Matrix 2026

Version 1.0.0. Snapshot date: 10 August 2026.

This release contains a reproducible, non-commercial evidence matrix for 2,742 United States vehicle model-years. It combines AutoWarranty's model-year mapping with dated National Highway Traffic Safety Administration complaint, recall and manufacturer-communication counts and exact-year FuelEconomy.gov configuration summaries.

Canonical research and methodology: https://autowarranty.autos/methodology

## Preserved release and mirrors

- Zenodo record and DOI: https://zenodo.org/records/22088240, DOI `10.5281/zenodo.22088240`
- Kaggle dataset: https://www.kaggle.com/datasets/finofin/autowarranty-vehicle-year-evidence-2026
- Hugging Face dataset: https://huggingface.co/datasets/finofin/autowarranty-vehicle-year-evidence-2026

These are Finofin-controlled distribution records for public access and reuse. They are not independent editorial endorsements.

## Files

- `data/vehicle-year-evidence.csv`: 2,742 model-year rows with NHTSA counts and, when available, exact-year EPA/DOE configuration summaries.
- `data/model-catalog.csv`: 323 model-level catalogue rows and snapshot totals.
- `data/epa-unmatched-model-years.csv`: 134 model-years without an exact FuelEconomy.gov match in this snapshot.
- `METHODOLOGY.md`: construction, joins and limitations.
- `DATA-DICTIONARY.md`: field definitions.
- `RIGHTS-AND-ATTRIBUTION.md`: source and reuse notes.
- `SHA256SUMS`: file integrity hashes.

## Important limitations

- Complaint counts are reports, not failure rates. Exposure, vehicle population and reporting behaviour are not normalised.
- Recall counts do not determine whether a specific VIN has an open recall. Check the official NHTSA VIN tool.
- Manufacturer communications are not recalls and may include service information, bulletins and other correspondence.
- EPA/DOE fields describe matched configurations, not the equipment fitted to every vehicle.
- Blank EPA fields mean no exact-year match in this snapshot. They must not be inferred.

No RepairPal-derived repair prices, modelled labour rates, affiliate fields, warranty scores, screenshots or provider recommendations are included.

## Citation

See `CITATION.cff`. Corrections can be reported through the public repository issue tracker or the AutoWarranty methodology page.

## Later research

[November 2026 research notes](NOVEMBER-2026-RESEARCH.md) link to separate studies of public contract wording and changes in NHTSA record counts. These pointers do not update the August 2026 dataset or extend its DOI, citation or license to the linked studies; the preserved August release remains unchanged.
