# Data dictionary

## `vehicle-year-evidence.csv`

- `snapshot_date`: AutoWarranty build date.
- `make`, `model`: curated display names.
- `make_slug`, `model_slug`: stable join keys.
- `model_year`: model year represented by the row.
- `fuel_family`: broad AutoWarranty catalogue family, not a configuration-level claim.
- `priority`: internal catalogue coverage tier retained for reproducibility, not a quality score.
- `nhtsa_recalls`: count of matched NHTSA recall records.
- `nhtsa_complaints`: count of matched NHTSA complaint records.
- `nhtsa_communications`: count of matched NHTSA manufacturer-communication records.
- `top_components_json`: JSON array of leading complaint components with counts and within-row shares.
- `epa_match_status`: whether an exact-year FuelEconomy.gov configuration match exists.
- `epa_configuration_count`: number of matched configurations.
- `vehicle_classes`, `fuel_options`, `drive_options`, `transmission_options`: pipe-separated distinct options across matched configurations.
- Low/high pairs: observed range across matched configurations for engine litres, cylinders, combined MPG, combined MPGe and electric range.
- Boolean availability fields: whether any matched configuration includes the feature.
- Source URL fields: official dataset landing pages.

## `model-catalog.csv`

One row per curated model with the covered-year range, record counts and EPA/DOE match coverage.

## `epa-unmatched-model-years.csv`

One row per curated model-year lacking an exact FuelEconomy.gov match in this snapshot. Absence is explicit and is not evidence that a vehicle or configuration does not exist.
