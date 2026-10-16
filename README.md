# Food and body-image themes in annotated social media posts

INFO 2950, Fall 2026

We study how food- and body-related concerns appear in two public annotation datasets: eating-disorder-related Twitter posts and the EDTT TikTok dataset. Phase II includes data cleaning, exploratory summaries, four figures, and two proposed analyses for the final report.

## Contributors

- Anya Choudhary
- Zara Islam (zsi2)
- Riya Gupta (rg823)
- April Vorontsova (vv252)

## Start here

- [Executed Phase II notebook](notebooks/INFO2950_Phase_II.ipynb)
- [Phase II PDF, Parts 1 and 2](reports/phase2/INFO2950_Phase_II.pdf)
- [HTML export](reports/phase2/INFO2950_Phase_II.html)
- [Raw source files and provenance](data/raw/)

## Research questions

1. What concerns and content features are recorded in each dataset, and how common are they among eligible posts?
2. Among Twitter posts coded as eating-disorder/body-image related, is a shape-concern annotation associated with an eating-concern annotation?
3. Within EDTT, is a restraint annotation associated with audio valence after accounting for post format?

Phase II explores the first question. Questions 2 and 3 are preregistered plans and have not been tested. These files describe post content. They do not establish algorithm effects, clinical diagnoses, or changes in viewers' food attitudes.

## Repository structure

```text
README.md                 Project overview and instructions
CONTRIBUTORS.md           Group member credits
requirements.txt          Versions used to execute the notebook
data/
  raw/                    Unchanged publisher files and checksums
  intermediate/           Validated and normalized snapshots
  processed/              Analysis tables and audit summaries
notebooks/                Executed Phase II Jupyter notebook
figures/                  Four exploratory figures
reports/
  phase1/                 Location reserved for the original Phase I submission
  phase2/                 Combined PDF and HTML exports
```

Each folder has a README explaining its contents. The original Phase I submission has not been provided and is not included; its folder README records that status.

## Data sources

- Cavazos-Rehg et al. (2019), [PLOS ONE article and supplements](https://doi.org/10.1371/journal.pone.0207506): 3,000 annotated Twitter posts collected in January 2015. The analysis retains 2,584 posts coded as related to eating disorders or body image.
- Shaveet, Viranda, and Choudhury (2026), [EDTT version 2](https://doi.org/10.5281/zenodo.19749827): 85 annotated TikTok posts. Six have blank EDE subscale annotations, which remain unknown in the derived indicators.

See [data/raw/README.md](data/raw/README.md) and [manifest.json](data/raw/manifest.json) for exact source files, download dates, and checksums. Source authors retain credit for the datasets; this project does not claim authorship of their data.

## Open in Google Colab

[Open the notebook in Colab](https://colab.research.google.com/github/AnyaChoudhary/info2950-fall2026-project/blob/main/notebooks/INFO2950_Phase_II.ipynb), then select **Runtime > Run all**. The first cell restores the four saved source files if they are missing. Internet access is required for that first restoration. It reuses the original project inputs rather than collecting new posts.

## Run the notebook locally

Use Python 3.12. From the repository root:

```bash
python3 -m venv .venv
source .venv/bin/activate
python -m pip install -r requirements.txt jupyterlab
jupyter lab notebooks/INFO2950_Phase_II.ipynb
```

On Windows, activate with `.venv\Scripts\activate` instead. Select the installed Python environment and choose **Restart Kernel and Run All**. The notebook finds the data folder automatically from either the repository root or `notebooks/`. No API key is needed. The full repository includes the data. When opened alone in Colab, the notebook restores the saved inputs from a pinned GitHub snapshot and verifies their checksums.

Execution verifies the raw-file checksums and recreates the intermediate files, processed files, and figures. It does not run either proposed inferential analysis. The PDF and HTML are saved exports of the executed notebook; rerunning cells alone does not regenerate those exports.

## Data handling

Twitter blanks caused by conditional coding remain blank. Eleven internally inconsistent Twitter records are flagged and retained. EDTT category indicators come from annotation headers; blank annotation fields remain unknown rather than becoming zeros. The two datasets are analyzed separately because their sampling and coding differ. The notebook documents these choices and their limitations.
