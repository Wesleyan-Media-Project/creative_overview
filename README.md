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

## Note on R and RData files From Markus Newman

RData files are the standard way of saving data in R. WMP uses them because 1) they are compressed by default, so they're smaller than csvs, and 2) because they retain information on data types. So for example, we have ad ids, which are numbers. So an ad id might be 2323532312. And if we save data as a csv and then reimport it, the importer makes some assumptions on each object's types, and sometimes it's wrong. This can cause those objects to be irreversibly mangled. To avoid that, in R, we tend to set them to strings, not integers (this is standard practice in computational social science). And if it is later loaded from an rdata file, it will know it's a string. Whereas if it is imported from a csv, it will usually think it's an integer, but depending on how high it is it will encode it as int16, int32, etc. and that can cause problems.

[Here are the results of some experiments with file compression of rdata and alternatives](https://github.com/Wesleyan-Media-Project/github_howto/wiki/File-compression)
