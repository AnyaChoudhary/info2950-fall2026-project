# Intermediate data

| File | Contents |
| --- | --- |
| `twitter_validated.csv` | All 3,000 original rows after column/type normalization and code/eligibility validation |
| `edtt_normalized.csv` | All 85 EDTT rows after normalized column names, whitespace trimming, numeric checks, and assignment of a local row ID; before category indicators |

These snapshots are recreated by Section 2 of the [notebook](../../notebooks/INFO2950_Phase_II.ipynb). Raw source files are preserved separately. Blank values remain blank in CSV form; the notebook uses nullable types during processing.
