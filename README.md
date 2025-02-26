# term-check
DHS has directed us to search for specific terms that must be removed from all DHS websites. This repo includes two jupyter notebooks to search `docx` documents and webpages for the presence of the terms supplied.

## Notebooks
1. `term-search_docx.ipynb` parses Word documents and indicates the presence or absence of a supplied list of terms.
2. `term-search_web.ipynb` scrapes webpages at a given domain and indicates the presence or absence of a supplied list of terms.

### Usage
For each notebook, reference the last section. Here's the section for `term-search_docx.ipynb`:

```
if __name__ == "__main__":
    docx_path = 'word_doc_here.docx'
    terms = ['Affirmative Action', 'DEI', 'DEIA', 'Diversity & Inclusion', 'Diversity and Inclusion', 'Diversity Equity & Inclusion', 'Diversity Equity and Inclusion', 'Diversity Equity and Inclusion', 'Diversity Equity Inclusion', 'Diversity Inclusion', 'Diversity, Equity & Inclusion', 'Diversity, Equity and Inclusion', 'Diversity, Equity Inclusion', 'Diversity, Equity, & Inclusion', 'Diversity, Equity, and Inclusion', 'Diversity, Equity, Inclusion', 'Equity & Diversity', 'Equity and Diversity', 'Gender Equality', 'Gender Equity', 'IDDP', 'Implicit Bias', 'Inclusion Diversity and Equity', 'Inclusion, Diversity and Equity', 'Inclusion, Diversity, Equity', 'Inclusive Diversity', 'LGBT', 'LGBTQ', 'LGBTQ+', 'LGBTQI', 'LGBTQIA', 'Racial Equality', 'Racial Equity', 'Social Justice', 'STEER', 'STRIDE', 'Unconscious Bias']
    counts = search_terms_in_docx(docx_path, terms)
    for term, count in counts.items():
        print(f"'{term}' found {count} times in the document.")
```

Replace `docx-path` with the path to your Word document. In `term-search_web.ipynb`, replace `domain` in this section with the full URL of the website you'd like to check.

## Text file
1. `terms.txt` includes the terms supplied by DHS that the scripts check for. The notebooks don't use this text file; rather, the notebooks include a python list with the terms. This `txt` file is only for reference, and includes the terms DHS sent to teams to remove from DHS websites.
