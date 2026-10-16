# Data

- [raw/](raw/): unchanged publisher downloads, the Twitter codebook, filtering rules, and provenance manifest.
- [intermediate/](intermediate/): complete validated/normalized snapshots created during cleaning.
- [processed/](processed/): analysis-ready tables and audit summaries created by the notebook.

Run [the Phase II notebook](../notebooks/INFO2950_Phase_II.ipynb) to reproduce intermediate and processed files. Do not edit raw inputs to correct annotation ambiguities. Record changes in the cleaning code and explain them in a markdown cell.

Twitter and TikTok remain separate datasets. There is no shared observation key or justified row-level merge.
