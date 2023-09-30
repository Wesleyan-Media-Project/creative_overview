# The Cross-platform Election Advertising Transparency Initiative (CREATIVE)

## About

The Cross-platform Election Advertising Transparency Initiative (CREATIVE), is a jointly founded infrastructure project by Wesleyan Media Project [(WMP)](https://mediaproject.wesleyan.edu) and [Privacy Tech Lab](https://privacytechlab.org) at Wesleyan University in Connecticut. This program is funded by a National Science Foundation [grant](https://www.nsf.gov/awardsearch/showAward?AWD_ID=2235006) to support making WMP’s work and data accessible to anyone. CREATIVE aims to provide cross-platform integration and standardization of digital advertising data related to federal elections by scraping or gaining access to digital ads themselves. (For more information on the CREATIVE project, click [here](https://www.creativewmp.com/)).

To that end, we have created several repositories to acquire, process and standardize digital election advertising data across platforms. These repositories are grouped into five steps:

- Step 1: Data Collection
- Step 2: Data Storage & Processing
- Step 3: Preliminary Data Classification
- Step 4: Final Data Classification
- Step 5: Data Output & Accessibility

Repositories defined in these steps do not neccesarily rely on a repository from a previous step. For example, the datasets repository found in step 2 does not rely on any repository in step 1, but does have repositories from step 1 that rely on data stored datasets like face_url_scrapper_2022. 

Below, you can find an overview of all repositories under the WMP organization belonging to the CREATIVE project. Also, check [Variable Wiki](https://github.com/Wesleyan-Media-Project/fb_entities_2020/wiki/Variable-Description) for clarity on acronyms. 

## Working Repositories

## Step 1: Data Collection

### [Face Collection 2022](https://github.com/Wesleyan-Media-Project/face_url_scraper_2022) (face_url_scraper_2022)

This is a Python-based web scraper that extracts images of political figures from URLs and saves the results in a CSV file.

### [Facebook Ad Scraper](https://github.com/Wesleyan-Media-Project/fb_ad_scraper) (fb_ad_scraper)

This repository provides the scripts that replicate the workflow used by the Wesleyan Media Project to collect the media (images and video) from Facebook ads.

### [Facebook Ads Import](https://github.com/Wesleyan-Media-Project/fb_ads_import) (fb_ads_imports)

Scripts used by the Wesleyan Media Project to import Facebook political ads.

### [Google Ads Archive](https://github.com/Wesleyan-Media-Project/google_ads_archive) 

Scripts used by the Wesleyan Media Project to import Google political ads.

### [Facebook Aggregate Reports Import](https://github.com/Wesleyan-Media-Project/fb_agg_reports_import) (fb_agg_reports_import)

Repository to collect and clean advertising reports from Facebook, ready to be analyzed.

### [Facebook Page Names](https://github.com/Wesleyan-Media-Project/fb_page_names) (fb_page_names)

Data and SQL scripts showing the history of changes in page names of FB advertisers. This repository describes the known problems with changes in page names of Facebook advertisers.

---
## Step 2: Data Storage & Processing

### [TV 2020 Data](https://github.com/Wesleyan-Media-Project/tv_2020) (tv_2022)

Data/ datasets and Readme only. Contains data over the election season period (09/01/2020 - 11/ 04/2020) and 4,058 ads.

### [Facebook Entities 2020](https://github.com/Wesleyan-Media-Project/fb_entities_2020) (fb_entities_2020)

Contains a readme about the 2020 FaceBook Entity files that describes where the Output files are and what variables type(FB, WMP, and CPR/OpenSecrets) are being used. Merges with the 1.18m fb_2020 repo data set (`02_fb_2020_118m_adid_var.ipynb`).

### [Datasets](https://github.com/Wesleyan-Media-Project/datasets)

This repository serves as a storage location for datasets used in other repositories.

### [Facebook 2020](https://github.com/Wesleyan-Media-Project/fb_2020) (fb_2020)

This repository contains codes that load, merge and process data from Facebook to create a comprehensive dataset for the 2020 Election cycle.

### [Facebook 2022](https://github.com/Wesleyan-Media-Project/fb_2022) (fb_2022)

This repository contains codes that load, merge and process data from Facebook to create a comprehensive dataset for the 2022 Election cycle.

### [Google 2022](https://github.com/Wesleyan-Media-Project/google_2022)

This repository contains codes that load, merge and process data from Google to create a comprehensive dataset for the 2022 Election cycle.

---
## Step 3: Preliminary Data Classification

### [Entity Linking 2020](https://github.com/Wesleyan-Media-Project/entity_linking) (entity_linking)

Identifying mentions of candidates (and other important politicians) in ad text for the 2020 Election cycle.

### [Entity Linking 2022](https://github.com/Wesleyan-Media-Project/entity_linking_2022)

This repository is an entity linker for 2022 election data. This entity linker was trained on data that contains descriptions of people and their names, along with their aliases. Data are sourced from the 2022 WMP persons file, and are restricted to general election candidates and other non-candidate persons of interest (sitting senators, cabinet members, international leaders, etc.)

### [Race of Focus](https://github.com/Wesleyan-Media-Project/race_of_focus)

This focuses on what political race the ad is about (based on what candidates are mentioned in the ad) and needs to use the entity linking program in order to find out. Only contains data files (rdata and csv)

### [Aspect-Based Sentiment Analysis](https://github.com/Wesleyan-Media-Project/ABSA) (ABSA)

This repository contains code for the Aspect-Based Sentiment Analysis (ABSA) project. The repository contains data, model and script for ABSA training.

---
## Step 4: Final Data Classification

### [Ad-level Party Classifier](https://github.com/Wesleyan-Media-Project/party_classifier) (party_classifier)

Multinomial party classifier, classifying ads into DEM/REP/OTHER. The difference to the Unique ID party classifier is that in this one, the training data consists of individual ads whose pd_id has party_all coded in the WMP entity file. By contrast, the Unique ID party classifier concatenates all ads of a pd_id into one.

### [Party Classifier with Unique ID](https://github.com/Wesleyan-Media-Project/party_classifier_pdid) (party_classifier_pdid)

Contains the steps to train the party classifier and links for training results. Model Performance (shown in a chart) looks for precision, recall, f1 score, and support for each party(republican, democrat, and other).

### [Ad Goal Classifier](https://github.com/Wesleyan-Media-Project/ad_goal_classifier)

The purpose of this repository is to classify the goals of advertisements across different data sources, including Facebook, TV, and Google. It involves a series of scripts that clean and prepare the data, train a machine learning model, and apply the trained model to different data sets for inference. 

### [Attack Like](https://github.com/Wesleyan-Media-Project/attack_like)

This repository contains the code for attack-like negativity measure for the 1.4m Facebook dataset: attacklike_fb2020_140m.csv

The classifier outputs class labels (Support/Attack) as well as class probabilities. The probabilities can be used to construct a 'Contrast' label.

### [Issue classifier](https://github.com/Wesleyan-Media-Project/issue_classifier)

Issue classifier, trained on 2018 and 2020 ads - both TV and Facebook, designed to be applied to uncoded 2022 ads. Based on WMP issue coding - not Kantar.

### [Ad Tone](https://github.com/Wesleyan-Media-Project/ad_tone)

This repository contains models to predict the tone of political ads. The main model "ad_tone_constructed" is based on this [flowchart](https://docs.google.com/presentation/d/11E9kX1oVYfMooTdD1GAJfwJtdPIQpYB3lJ7i5e83ZEw/edit#slide=id.g1062def0ba3_0_0).

---
## Step 5: Data Output & Accessibility

### [Public Data](https://github.com/Wesleyan-Media-Project/public_data)

Contains a readme (.md file) that describes how to access data released by Facebook from the Wesleyan Media Project. "One-off release of specific data" can be granted with citation notes.

---



### [Github How to Instructions](https://github.com/Wesleyan-Media-Project/github_howto)

Instructions on Github from wiki that goes over needed elements, like: git pull, push, merge, and commit in order to use GitHub. Folder structure instructions are also in the wiki link.

---
## Note on R and RData files From Markus Neumann:

RData files are the standard way of saving data in R. WMP uses them because 1) they are compressed by default, so they're smaller than csvs, and 2) because they retain information on data types. So for example, we have ad ids, which are numbers. So an ad id might be 2323532312. And if we save data as a csv and then reimport it, the importer makes some assumptions on each object's types, and sometimes it's wrong. This can cause those objects to be irreversibly mangled. To avoid that, in R, we tend to set them to strings, not integers (this is standard practice in computational social science). And if it is later loaded from an rdata file, it will know it's a string. Whereas if it is imported from a csv, it will usually think it's an integer, but depending on how high it is it will encode it as int16, int32, etc. and that can cause problems.

[Here are the results of some experiments with file compression of rdata and alternatives](https://github.com/Wesleyan-Media-Project/github_howto/wiki/File-compression)
