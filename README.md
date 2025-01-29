# dhs-term-search
DHS has directed us to search for specific terms that must be removed from DHS websites. This repo includes two jupyter notebooks to search `docx` documents and webpages for the presence of the terms supplied.

## Notebooks
1. `term-search_docx.ipynb` parses Word documents and indicates the presence or absence of a supplied list of terms.
2. `term-search_web.ipynb` scrapes webpages at a given domain and indicates the presence or absence of a supplied list of terms.

## Text file
1. `terms.txt` includes the terms supplied by DHS that the scripts check for. The notebooks don't use this text file; rather, the notebooks include a python list with the terms. This `txt` file is only for reference, and includes the terms DHS sent to teams to remove from DHS websites.
