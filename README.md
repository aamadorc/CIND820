
# Background

The Coronavirus disease (COVID-10) was first reported in December, 2019 in
Wuhan, Hubei Province, China. It created a calamitous situation throughout the
world as cumulative incidents of COVID-19 increased day by day. In the absence
of any medications, the only solution was to slow down the spread by exercising
“social distancing”, which included hard lock-downs, restrictions on people
mobility, limitations of the number of people in public places and the usage of
protection gear including masks or gloves, to block the chain of the spread of
the virus. This is where Machine Learning models help forecast where and when 
the disease is likely to spread, and notify those regions, governments and
entities on their decision making.

# Datasets

This dataset is taken from Our World in Data website, officially collected by Our World in Data team. This dataset is synced daily:

https://covid.ourworldindata.org/data/owid-covid-data.csv. 

These are the following information included in the dataset:

| Metrics | Source | Updated | Countries |
| -- | -- | -- | -- |
| Vaccinations | Official data collated by the Our World in Data team | Daily | 218 |
| Tests & positivity | Official data collated by the Our World in Data team | Weekly | 139 |
| Hospital & ICU | Official data collated by the Our World in Data team | Weekly | 39 |
| Confirmed cases | JHU CSSE COVID-19 Data | Daily | 196 |
| Confirmed deaths | JHU CSSE COVID-19 Data | Daily | 196 |
| Reproduction rate | Arroyo-Marioli F, Bullano F, Kucinskas S, Rondón-Moreno C | Daily | 185 |
| Policy responses | Oxford COVID-19 Government Response Tracker | Daily | 186 |
| Other variables of interest | International organizations (UN, World Bank, OECD, IHME…) | Fixed | |

The dataset is available to the Kaggle community:
https://www.kaggle.com/datasets/caesarmario/our-world-in-data-covid19-dataset

# Reproducibility

## Python Environment

`requirements.txt` is included in this repository to set up a Python virtual
environment with the version of all required packages used.

For example:
```bash
python -m venv .venv
.venv\Scripts\activate.bat
pip install -r requirements.txt
```

Once completed, load the notebook and change the Jupyter Kernel to `python`
in the `.venv\Scripts` directory.

# Browsing the Timeline of Changes

The Jupyter Notebooks in the repository include the data in them, but
additionally HTML exports are included every time the source Notebook changes.
It is possible to review how the individual files change over time, but in
order to make this navigation easier a GitHub Action is included to maintain the
GitHub Page associated with the repository. For reference, see
[.github/workflows/gh-pages.yml](.github/workflows/gh-pages.yml),
[generate-extra-docs.py](generate-extra-docs.py) and
[mkdocs.yml](mkdocs.yml).

The resulting GitHub Page is located at [.github/workflows/gh-pages.yml](.github/workflows/gh-pages.yml).

# Files in the Repository

| File | Description |
| ---- | ---- |
| [.gitattributes](.gitattributes) | Set atributes for LFS stored files so that they can be easily viewed and diff-ed. |
| [.github/workflows/gh-pages.yml](.github/workflows/gh-pages.yml) | GitHub action to update [https://github.io/aamadorc/CIND820](https://aamadorc.github.io/CIND820/) on pushes to the repository. |
| [.gitignore](.gitignore) | Files and file patterns that I want git to ignore. |
| [CIND820\_EDA.html](CIND820\_EDA.html) | HTML export of the main Jupyter notebook. In the history of this file, the first commit includes the data profiling of the complete dataset. |
| [CIND820\_EDA.ipynb](CIND820\_EDA.ipynb) | Main Jupyter notebook with the code. |
| [CIND820\_EDA\_subset.html](CIND820\_EDA\_subset.html) | HTML export of Jupyter notebook with code of the data profiling of a subset of the dataset. |
| [CIND820\_EDA\_subset.ipynb](CIND820\_EDA\_subset.ipynb) | Jupyter notebook with code of the data profiling of a subset of the dataset.|
| [CND820\_LiteratureReview\_AngelaAmador.docx](CND820\_LiteratureReview\_AngelaAmador.docx) | Literature Review document. |
| [README.md](README.md) | This file. |
| [archive.zip](archive.zip) | Dataset from Our World in Data website. |
| [generate-extra-docs.py](generate-extra-docs.py) | Helper script to generate markdown with the list of changes to the HTML exports in the repository, and dump those files. The website is made up of this markdown plus README.md, and converted into HTML using [mkdocs](https://www.mkdocs.org).<br/>This is invoked by the GitHub action. |
| [mkdocs.yml](mkdocs.yml) | Configuration file for mkdocs.<br/>mkdocs is invoked from the GitHub action. |
| [requirements-docs.txt](requirements-docs.txt) | Pip requirements file for the packages required by the GitHub action. |
| [requirements.txt](requirements.txt) | Pip requirements file for the packages required by the code in the Jupyter notebooks. |