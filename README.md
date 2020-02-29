# BIDMC Datathon (29 February 2020)

This repository contains resources for the BIDMC Datathon 2020.

## Contents

1. Getting started
2. Documentation
3. Databases on BigQuery
4. Analysing data with Google Colab
5. Notebooks that we prepared earlier
6. Sample projects

## 1. Getting started

The datasets are hosted on Google Cloud, which requires a Gmail account to manage permissions.

1. Create a [Gmail account](https://www.google.com/gmail/about/), if you don't already have one. It will be used to manage your access to the resources.
2. Give your gmail address to the session hosts.

## 2. Documentation

We will be working with two critical care datasets during the event: [MIMIC-III](https://mimic.physionet.org/) and the [eICU Collaborative Research Database](https://eicu-crd.mit.edu/).

- MIMIC-III Clinical Database: https://mimic.physionet.org/
- eICU Collaborative Research Database: https://eicu-crd.mit.edu/

## 3. Databases on BigQuery

BigQuery is a database system that makes it easy to explore data with Structured Query Language ("SQL"). There are several datasets on BigQuery available for you to explore, including `eicu_crd` (the eICU Collaborative Research Database) and `mimiciii_clinical` (the MIMIC-III Clinical Database).

You will also find "derived" databases, which include tables derived from the original data using the code in the [eICU](https://github.com/MIT-LCP/eicu-code) and [MIMIC](https://github.com/MIT-LCP/mimic-code) code repositories. These are helpful if you are looking for something like a sepsis cohort or first day vital signs.

1. [Open BigQuery](https://console.cloud.google.com/bigquery?project=bidmc-datathon).
2. At the top of the console, select `bidmc-datathon` as the project. This indicates the account used for billing.
3. "Pin" a project to the resources menu to view available datasets. In the Resources menu on the left, click "Add data", "Pin a project", then add the following project names: `physionet-data` and `bidmc-datathon`.
4. You should be able preview the data available on these projects using the graphical interface.
5. Now try running a query. For example, try counting the number of rows in the demo eICU patient table:

   ```SQL
   SELECT count(*)
   FROM `physionet-data.eicu_crd_demo.patient` 
   ```

## 4. Analysing data with Google Colab

Python is an increasingly popular programming language for analysing data. We will explore the data using Python notebooks, which allow code and text to be combined into executable documents. First, try opening a blank document using the link below:

- [https://colab.research.google.com/](https://colab.research.google.com/)

## 5. Python and R notebooks that we prepared earlier

Several tutorials are provided below. Requirements for these notebooks are: (1) you have a Gmail account and (2) your Gmail address has been added to the appropriate Google Group by the workshop hosts.

BIDMC Q1: Data extraction for the English vs. Non-English Speaker project (MIMIC/R) <a href="https://colab.research.google.com/github/MIT-LCP/bidmc-datathon/blob/master/inference_01_extraction.ipynb" target="_parent"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/></a>

BIDMC Q1: Exploratory analysis in English vs. Non-English Speakers (MIMIC/Python) <a href="https://colab.research.google.com/github/MIT-LCP/bidmc-datathon/blob/master/inference_02_analysis.ipynb" target="_parent"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/></a>

BIDMC Q1: Exploratory analysis in English vs. Non-English Speakers (MIMIC/R) <a href="https://colab.research.google.com/github/MIT-LCP/bidmc-datathon/blob/master/inference_02_analysisR.ipynb" target="_parent"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/></a>

Exploring the patient table (eICU): <a href="https://colab.research.google.com/github/MIT-LCP/bidmc-datathon/blob/master/01_explore_patients.ipynb" target="_parent"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/></a>

Severity of illness (eICU): <a href="https://colab.research.google.com/github/MIT-LCP/bidmc-datathon/blob/master/02_severity_of_illness.ipynb" target="_parent"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/></a>

Summary statistics (eICU) <a href="https://colab.research.google.com/github/MIT-LCP/bidmc-datathon/blob/master/03_summary_statistics.ipynb" target="_parent"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/></a>

Timeseries for a single patient (eICU) <a href="https://colab.research.google.com/github/MIT-LCP/bidmc-datathon/blob/master/04_timeseries.ipynb" target="_parent"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/></a>

Mortality prediction (eICU) <a href="https://colab.research.google.com/github/MIT-LCP/bidmc-datathon/blob/master/05_mortality_prediction.ipynb" target="_parent"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/></a>

Acute kidney injury (eICU) <a href="https://colab.research.google.com/github/MIT-LCP/bidmc-datathon/blob/master/06_aki_project.ipynb" target="_parent"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/></a>

Weekend effect on mortality (MIMIC) <a href="https://colab.research.google.com/github/MIT-LCP/bidmc-datathon/blob/master/mimic-weekend-effect.ipynb" target="_parent"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/></a>

Project work (eICU) <a href="https://colab.research.google.com/github/MIT-LCP/bidmc-datathon/blob/master/07_project_work.ipynb" target="_parent"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/></a>

## 6. Sample projects

These papers and repositories may be helpful for reference. They are definitely **not** perfect! Code may be untidy, poorly documented, buggy, outdated etc. Think about how they can be improved, adapted, etc. For example, you could:

- replicate the study on a different dataset (e.g. MIMIC vs eICU)
- improve the methodology

1. The association between mortality among patients admitted to the intensive care unit on a weekend compared to a weekday

- Python Notebook: https://github.com/MIT-LCP/bhi-bsn-challenge/blob/master/challenge-demo.ipynb
- R Markdown Notebook: https://github.com/MIT-LCP/bhi-bsn-challenge/blob/master/rmarkdown_example_notebook.Rmd
- More reading: https://physionet.org/content/bhi-2018-challenge/1.0/

To be continued...