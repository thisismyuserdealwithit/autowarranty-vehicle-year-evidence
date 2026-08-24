# Methodology

## Scope and dates

The release is a dated snapshot of the public-data layer used by AutoWarranty. The AutoWarranty data build is dated 10 August 2026. The FuelEconomy.gov configuration snapshot is dated 7 August 2026.

## Construction

1. AutoWarranty's curated model catalogue defines the 323 make/model entities and their covered model years.
2. NHTSA-derived complaint, recall and manufacturer-communication records are grouped by the curated make, model and model year.
3. Component counts are retained as a JSON array for the leading complaint components associated with each row.
4. FuelEconomy.gov configurations are matched only when the curated `make_slug`, `model_slug` and exact model year match the configuration snapshot.
5. Multiple matching configurations are summarised as counts, distinct categorical options and low/high numeric ranges.
6. Model-years without an exact configuration match remain blank in the main matrix and are listed separately. No values are imputed.

## Quality controls

- Exactly 2,742 model-year records are required.
- Exactly 323 model-catalogue records are required.
- Exactly 134 unmatched EPA/DOE model-years are required.
- The three tables total 3,199 rows, excluding headers.
- Each model-year key is unique.
- Numeric counts must be non-negative integers.
- Match status must be `matched` or `unmatched`; unmatched rows must not contain EPA configuration values.
- Repair prices, warranty classifications, affiliate data and other commercial fields are excluded.

## Interpretation

The release measures record counts within the source snapshot. It is not a reliability ranking, incidence rate, recall-status lookup or warranty recommendation. Cross-model comparisons should account for fleet size, age, sales volume and reporting behaviour, none of which is normalised here.

## Source refreshes

Future releases should increment the version, preserve the earlier release, record new source dates, rerun the uniqueness and count checks, and document mapping changes in `CHANGELOG.md`.
