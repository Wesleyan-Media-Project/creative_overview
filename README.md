# creative_overview

An overview of all repos belonging to the CREATIVE project
Also check [Variable Wiki](https://github.com/Wesleyan-Media-Project/fb_entities_2020/wiki/Variable-Description) for clarity on acronyms.

## Summary of Working Repositories

### [Issue classifier](https://github.com/Wesleyan-Media-Project/issue_classifier)

> **Summary**
> Applied to uncoded ads in order to sort them. Uses two different binary classifiers in order to sort through ads, since they can have multiple problems: binary (higher precision, lower recall) and multilabel (higher F1 score). Binary classifier is used for issues with missing data, multilabel with none missing. Deals separately with digital media model training on Facebook data then imputing the missing FB data. Using 65 issues.

> **Important Notes**
> Problems in issue coding that need to be updated in issue_coding folder, classifying issues that occurred at least 100 times, but excluding problematic issues 116 and 206

> **Languages, Files, and others**
> R, Python, Jupyter Notebook, RData file (RStudio), dta file, ipynb file, csv(comma-separated values) file, xlsx (microsoft excel spreadsheet) file, txt, json file, google ASR

### [Party Classifier with Unique ID](https://github.com/Wesleyan-Media-Project/party_classifier_pdid)

> **Summary**
> Contains the steps to train the party classifier and links for training results. Model Performance (shown in a chart) looks for precision, recall, f1 score, and support for each party(republican, democrat, and other).

> **Important Notes**
> N/A

> **Languages, Files, and others**
> Jupyter notebook

### [Entity Linking](https://github.com/Wesleyan-Media-Project/entity_linking)

> **Summary**
> Contains Google code, data, and results and FaceBook code and data. These are paths for training. Trains the machine on the dataset of the candidates (id(qid), name, aliases, and description)

> **Important Notes**
> No results, yet, for FaceBook

> **Languages, Files, and others**
> R, Python, md, txt, csv, rdata, gz, dta

### [Race of Focus](https://github.com/Wesleyan-Media-Project/race_of_focus)

> **Summary**
> This focuses on what political race the ad is about (based on what candidates are mentioned in the ad) and needs to use the entity linking program in order to find out. Only contains data files (rdata and csv)

> **Important Notes** > `Race_of_focus_textonly.R` not up to date

> **Languages, Files, and others**
> R language only, csv, rdata

### [Public Data](https://github.com/Wesleyan-Media-Project/public_data)

> **Summary**
> Contains a readme (.md file) that describes how to access data released by Facebook from the Wesleyan Media Project. "One-off release of specific data" can be granted with citation notes.

> [Notes on Data Release](https://github.com/Wesleyan-Media-Project/public_data/releases)

> [Available releases](https://github.com/Wesleyan-Media-Project/public_data/releases/tag/fb2020_weekly_agg_v1)

> [Data prior than 2020 and Kantar](https://mediaproject.wesleyan.edu/dataaccess/)

> **Important Notes**
> N/A

> **Languages, Files, and others**
> N/A

### [TV 2020 Data](https://github.com/Wesleyan-Media-Project/tv_2020)

> **Summary**
> Data/ datasets and Readme only. Contains data over the election season period (09/01/2020 - 11/ 04/2020) and 4,058 ads.

> **Important Notes** > `tv_2020_fed.ipynb` contains warning

> **Languages, Files, and others**
> Jupyter Notebook, csv, dta, ipynb, google ASR, AWS face recognition

### [Github How to Instructions](https://github.com/Wesleyan-Media-Project/github_howto)

> **Summary**
> Instructions on Github from wiki that goes over needed elements, like: git pull, push, merge, and commit in order to use GitHub. Folder structure instructions are also in the wiki link.

> **Important Notes**
> Can clean up files like `test.txt`

> **Languages, Files, and others**
> png files for visual explanations

### [Facebook Entities](https://github.com/Wesleyan-Media-Project/fb_entities_2020)

> **Summary**
> Contains a readme about the 2020 FaceBook Entity files that describes where the Output files are and what variables type(FB, WMP, and CPR/OpenSecrets) are being used. Merges with the 1.18m fb_2020 repo data set (`02_fb_2020_118m_adid_var.ipynb`).

> **Important Notes**
> N/A

> **Languages, Files, and others**
> No languages, but the readme references csv

### [Party Classifier](https://github.com/Wesleyan-Media-Project/party_classifier)

> **Summary**
> Contains code for Party classifier that uses the 1.18m FB dataset (`02_fb_2020_118m_adid_var.ipynb`) and trains on a portion of the data. In training, the data is in a 70:30 split to training and test, respectively. Shows the data and results links and performance table. Classifier is logistic regression so not all probabilities are either >0.99 or <0.01.

> **Important Notes**
> In `model_history.txt` describes remaining issues with classifiers, `original_query.txt` no longer used, do not currently only deduplicate within page_ids (currently deduplicate every concatenated ad)

> **Languages, Files, and others**
> Python, R, csv, gitnore, joblib file(for training models)

---
## [face_url_scraper_2022](https://github.com/Wesleyan-Media-Project/face_url_scraper_2022)
`face_url_scraper_2022` is a Python-based web scraper that extracts images of political figures from URLs and saves the results in a CSV file.

### Dependencies
Some scripts run in a Python environment using Jupyter Notebook and require the following packages:
- pandas
- numpy
- bs4
- urllib
- re
- fuzzywuzzy

In addition, some parts of the code require R to be installed, along with the following R packages:
- tidyverse
- rvest
- httr
- xml2

---

## [datasets](https://github.com/Wesleyan-Media-Project/datasets)

`datasets` serves as a storage location for datasets used in other repositories.

### Some other repositories that use this repository
- [forum_digital_2022](https://github.com/Wesleyan-Media-Project/forum_digital_2022)
- [ad_goal_classifier](https://github.com/Wesleyan-Media-Project/ad_goal_classifier)
- [ad_tone](https://github.com/Wesleyan-Media-Project/ad_tone)
- [forum_digital_2022](https://github.com/Wesleyan-Media-Project/forum_digital_2022)
- [ad_goal_classifier](https://github.com/Wesleyan-Media-Project/ad_goal_classifier)
- [ABSA](https://github.com/Wesleyan-Media-Project/ABSA)
- [entity_linking_2022](https://github.com/Wesleyan-Media-Project/entity_linking_2022)
- [race_of_focus](https://github.com/Wesleyan-Media-Project/race_of_focus)
- [issue_classifier](https://github.com/Wesleyan-Media-Project/issue_classifier)
- [party_classifier](https://github.com/Wesleyan-Media-Project/party_classifier)
### Dependencies
 Some parts of the code in `datasets` require R to be installed, along with the following R libraries:
 - data.table
 - dplyr
 - tidyr 
 - stringr

 ---
## [entity_linking_2022](https://github.com/Wesleyan-Media-Project/entity_linking_2022)
 This repository is an entity linker for 2022 election data. This entity linker was trained on data that contains descriptions of people and their names, along with their aliases. Data are sourced from the 2022 WMP persons file, and are restricted to general election candidates and other non-candidate persons of interest (sitting senators, cabinet members, international leaders, etc.)

### Dependencies
Some scripts run in a Python environment require the following packages:
- csv
- pathlib
- os
- random
- json
- pandas
- spacy (***requires version 3.2***)
- en_core_web_lg from spacy (***requires manual instalation through `python -m spacy download en_core_web_lg`***)
- KnowledgeBase from spacy.kb
- minibatch and compounding from spacy.util
- tqdm
- numpy
- Example from spacy.training
- load_kb from spacy.ml.models

In addition, some parts of the code require R to be installed, along with the following R libraries: 
- dplyr
- data.table
- haven
- stringr
- stringi
- quanteda
- tidyr

---
## [ABSA](https://github.com/Wesleyan-Media-Project/ABSA)

This repository contains code for the Aspect-Based Sentiment Analysis (ABSA) project. The repository contains data, model and script for ABSA training. The classification report generated by script "02_train_rf_118m.py" shows that the ABSA model has an overall accuracy of 0.81, with a macro average f1-score of 0.68.

### Dependencies
Some scripts run in a Python environment require the following packages:
- pandas
- sklearn.feature_extraction.text
- sklearn.ensemble (requires `RandomForestClassifier` and `Pipeline` )
- sklearn
- joblib

In addition, some parts of the code require R to be installed, along with the following R libraries: 
- data.table
- tidyr
- stringi
- stringr
- dplyr

---
## [ad_tone](https://github.com/Wesleyan-Media-Project/ad_tone)

This repository contains models to predict the tone of political ads. The main model "ad_tone_constructed" is based on this [flowchart](https://docs.google.com/presentation/d/11E9kX1oVYfMooTdD1GAJfwJtdPIQpYB3lJ7i5e83ZEw/edit#slide=id.g1062def0ba3_0_0).
### Dependencies
 To run the script that constructs this variable, the following packages are required:
 - [ABSA](https://github.com/Wesleyan-Media-Project/ABSA), 
 - [race of focus](https://github.com/Wesleyan-Media-Project/race_of_focus),
- candidates dataset
- `mention-based ad tone` 

In addition, some parts of the code require R to be installed, along with the following R libraries: 
- data.table
- tidyverse
- dplyr
- purrr
- stringr

---
## [ad_goal_classifier](https://github.com/Wesleyan-Media-Project/ad_goal_classifier)
The purpose of this repository is to classify the goals of advertisements across different data sources, including Facebook, TV, and Google. It involves a series of scripts that clean and prepare the data, train a machine learning model, and apply the trained model to different data sets for inference. 

For more details on the project pipeline, refer to the [README](https://github.com/Wesleyan-Media-Project/ad_goal_classifier/blob/main/README.md) in the repository.

### Dependencies
Some scripts run in a Python environment require the following packages:
- sklearn
- pandas
- numpy
- joblib

You can install these libraries by running the following command:

`pip install scikit-learn pandas numpy joblib`

In addition, some parts of the code require R to be installed, along with the following R libraries:
- data.table
- stringr
- stringi
- dplyr
- tidyr

---
## [attack_like](https://github.com/Wesleyan-Media-Project/attack_like)
This repository contains code for an attack-like negativity measure applied to the 1.18 million Facebook dataset "fb_2020_attacklike.csv". The classifier outputs class labels of either "Support" or "Attack" as well as class probabilities, which can be used to create a "Contrast" label. The classifier is trained on 7,949 political advertisements from a 2018 Facebook data set and uses a pre-trained DistilBERT base model to fine-tune the model for the classification of ad tone. 

For more details on the classifier, refer to the [README](https://github.com/Wesleyan-Media-Project/attack_like#readme) in the repository.


The code "1_embed_apsr.py" is about sentiment analysis of text data using the BERT (Bidirectional Encoder Representations from Transformers) model. The goal of this code is to build a model to predict the sentiment (either Attack, Promote or Contrast) of the text based on its content. The following packages are required to run this code:

- numpy
- pandas
- pickle
- scikit-learn
- torch
- transformers

"2_embed_fb2020.py" preprocesses a Facebook ad dataset and extracts sentiment embeddings from the ad texts using the Pretrained DistilBERT Model by huggingface (Transformers library).
This code requires the following Python packages:

- numpy
- pandas
- torch
- transformers
- warnings
- time

---
## [fb_2020](https://github.com/Wesleyan-Media-Project/fb_2020)
This repository contains codes that load, merge and process data from multiple sources to create a single comprehensive dataset.The data sets are in the form of CSV (Comma-Separated Value) files, and the code uses the Pandas library to load and manipulate them. More information about the datasets, variables and output files can be found in the [README](https://github.com/Wesleyan-Media-Project/fb_2020#readme)

### Dependencies
Some scripts run in a Python environment using Jupyter Notebook and require the following packages:
- pandas
- numpy
- ast
- re


## Note on R and RData files From Markus Newman

RData files are the standard way of saving data in R. WMP uses them because 1) they are compressed by default, so they're smaller than csvs, and 2) because they retain information on data types. So for example, we have ad ids, which are numbers. So an ad id might be 2323532312. And if we save data as a csv and then reimport it, the importer makes some assumptions on each object's types, and sometimes it's wrong. This can cause those objects to be irreversibly mangled. To avoid that, in R, we tend to set them to strings, not integers (this is standard practice in computational social science). And if it is later loaded from an rdata file, it will know it's a string. Whereas if it is imported from a csv, it will usually think it's an integer, but depending on how high it is it will encode it as int16, int32, etc. and that can cause problems.

[Here are the results of some experiments with file compression of rdata and alternatives](https://github.com/Wesleyan-Media-Project/github_howto/wiki/File-compression)
