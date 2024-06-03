# The Cross-platform Election Advertising Transparency Initiative (CREATIVE)

## About
Welcome! This repo contains information about and links to the various repositories that make up the CREATIVE project. We hope that through having a centralized overview page, we are making navigating this project more accessible for journalists, academic researchers, and others interested in the democratic process. 

The Cross-platform Election Advertising Transparency Initiative (CREATIVE), is a jointly founded infrastructure project by Wesleyan Media Project [(WMP)](https://mediaproject.wesleyan.edu) and [Privacy Tech Lab](https://privacytechlab.org) at Wesleyan University in Connecticut. This program is funded by a National Science Foundation [grant](https://www.nsf.gov/awardsearch/showAward?AWD_ID=2235006) to support making WMP’s work and data accessible to anyone. CREATIVE aims to provide cross-platform integration and standardization of digital advertising data related to federal elections by scraping or gaining access to digital ads themselves. (For more information on the CREATIVE project, click [here](https://www.creativewmp.com/)).

To that end, we have created several repositories to acquire, process and standardize digital election advertising data across platforms. These repositories are grouped into five steps:

- [Step 0: Overview](https://github.com/Wesleyan-Media-Project/creative_overview)
- [Step 1: Data Collection](https://github.com/Wesleyan-Media-Project/creative_overview/tree/main#step-1-data-collection)
- [Step 2: Data Processing](https://github.com/Wesleyan-Media-Project/creative_overview/tree/main#step-2-data-processing)
- [Step 3: Data Classification](https://github.com/Wesleyan-Media-Project/creative_overview/tree/main#step-3-data-classification)
- [Step 2a/3a: Data Merging](https://github.com/Wesleyan-Media-Project/creative_overview/tree/main#step2a/3a-data-merging)
- [Step 4: Compiled Final Data](https://github.com/Wesleyan-Media-Project/creative_overview/tree/main#step-4-compiled-final-data)

Repositories defined in these steps do not neccesarily rely on a repository from a previous step. For example, the datasets repository found in step 2 does not rely on any repository in step 1, but does have repositories from step 1 that rely on data stored datasets like face_url_scrapper_2022. 

Below, you can find an overview of all repositories under the WMP organization belonging to the CREATIVE project. Also, check [Variable Wiki](https://github.com/Wesleyan-Media-Project/fb_entities_2020/wiki/Variable-Description) for clarity on acronyms. 

![A picture of the pipeline diagram](CREATIVE_032524.png)
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

### [Facebook PD ID](https://github.com/Wesleyan-Media-Project/fb_pd_id) (fb_pd_id)

This repository provides the scripts for generating the FB identity ids - pd ids - used by WMP.

---
## Step 2: Data Processing

### [Image Vido Data Preparation](https://github.com/Wesleyan-Media-Project/image-video-data-preparation) (image-video-data-preparation)

This repository contains code that allows for selecting and preprocessing image and video data for the AWS Rekognition pipeline, as well as querying text ads data.

### [Automatic Speech Recognition](https://github.com/Wesleyan-Media-Project/automatic-speech-recognition) (automatic-speech-recognition)

This repo contains codes that replicate the workflow used by the Wesleyan Media Project to perform automatic speech recognition (ASR) on political ad videos.

### [AWS Rekognition Image Video Processing](https://github.com/Wesleyan-Media-Project/aws-rekognition-image-video-processing) (aws-rekognition-image-video-processing)

This repository contains code that replicates the workflow used by the Wesleyan Media Project to perform image and video recogonition on political ads through the Amazon Rekognition service (AWS SDK for Python).

---
## Step 3: Data Classification

### [Entity Linking 2022](https://github.com/Wesleyan-Media-Project/entity_linking_2022)

This repository is an entity linker for 2022 election data. This entity linker was trained on data that contains descriptions of people and their names, along with their aliases. Data are sourced from the 2022 WMP persons file, and are restricted to general election candidates and other non-candidate persons of interest (sitting senators, cabinet members, international leaders, etc.)

### [Race of Focus](https://github.com/Wesleyan-Media-Project/race_of_focus)

This focuses on what political race the ad is about (based on what candidates are mentioned in the ad) and needs to use the entity linking program in order to find out. Only contains data files (rdata and csv)

### [Aspect-Based Sentiment Analysis](https://github.com/Wesleyan-Media-Project/ABSA) (ABSA)

This repository contains code for the Aspect-Based Sentiment Analysis (ABSA) project. The repository contains data, model and script for ABSA training.

### [Ad Tone](https://github.com/Wesleyan-Media-Project/ad_tone)

This repository contains models to predict the tone of political ads.

### [Party Classifier with Unique ID](https://github.com/Wesleyan-Media-Project/party_classifier_pdid) (party_classifier_pdid)

Contains the steps to train the party classifier and links for training results. Model Performance looks for precision, recall, f1 score, and support for each party (Republican, Democrat, and Other).

### [Ad-level Party Classifier](https://github.com/Wesleyan-Media-Project/party_classifier) (party_classifier)

Multinomial party classifier, classifying ads into DEM/REP/OTHER. The difference to the Unique ID party classifier is that in this one, the training data consists of individual ads whose pd_id has party_all coded in the WMP entity file. By contrast, the Unique ID party classifier concatenates all ads of a pd_id into one.

### [Attack Like](https://github.com/Wesleyan-Media-Project/attack_like)

This repository contains the code for attack-like negativity measure for the Facebook and Google datasets.

The classifier outputs class labels (Support/Attack) as well as class probabilities. The probabilities can be used to construct a 'Contrast' label.

### [Ad Goal Classifier](https://github.com/Wesleyan-Media-Project/ad_goal_classifier)

The purpose of this repository is to classify the goals of advertisements across different data sources, including Facebook, TV, and Google. It involves a series of scripts that clean and prepare the data, train a machine learning model, and apply the trained model to different data sets for inference. 

### [Issue classifier](https://github.com/Wesleyan-Media-Project/issue_classifier)

Issue classifier, trained on 2018 and 2020 ads - both TV and Facebook, designed to be applied to uncoded 2022 ads. Based on WMP issue coding - not Kantar.


---
## Step 2a/3a: Data Merging
### [Data Post Production](https://github.com/Wesleyan-Media-Project/data-post-production)

This repo contains code that allows for merging different data fields and final data cleaning.

---
## Step 4: Compiled Final Data
### [Datasets](https://github.com/Wesleyan-Media-Project/datasets)

This repository is meant as a place to store datasets whose creation isn't assumed to be replicable (but which are used as inputs to other things that are meant to be replicable from that point on).

### [Facebook Page Names](https://github.com/Wesleyan-Media-Project/fb_page_names) (fb_page_names)
This repository contains data and SQL scripts showing the history of changes in page names of FB advertisers. This repository describes the known problems with changes in page names of Facebook advertisers.

---
## Note on R and RData files From Markus Neumann:

RData files are the standard way of saving data in R. WMP uses them because 1) they are compressed by default, so they're smaller than csvs, and 2) because they retain information on data types. So for example, we have ad ids, which are numbers. So an ad id might be 2323532312. And if we save data as a csv and then reimport it, the importer makes some assumptions on each object's types, and sometimes it's wrong. This can cause those objects to be irreversibly mangled. To avoid that, in R, we tend to set them to strings, not integers (this is standard practice in computational social science). And if it is later loaded from an rdata file, it will know it's a string. Whereas if it is imported from a csv, it will usually think it's an integer, but depending on how high it is it will encode it as int16, int32, etc. and that can cause problems.

[Here are the results of some experiments with file compression of rdata and alternatives](https://github.com/Wesleyan-Media-Project/github_howto/wiki/File-compression)


## Thank You

<p align="center"><strong>We would like to thank our financial supporters!</strong></p><br>

<p align="center">This material is based upon work supported by the National Science Foundation under Grant Numbers 2235006, 2235007, and 2235008.</p>

<p align="center" style="display: flex; justify-content: center; align-items: center;">
  <a href="https://www.nsf.gov/awardsearch/showAward?AWD_ID=2235006">
    <img class="img-fluid" src="nsf.png" height="150px" alt="National Science Foundation Logo">
  </a>
</p>

<p align="center">The Cross-Platform Election Advertising Transparency Initiative (CREATIVE) is a joint infrastructure project of the Wesleyan Media Project and privacy-tech-lab at Wesleyan University in Connecticut.

<p align="center" style="display: flex; justify-content: center; align-items: center;">
  <a href="https://www.creativewmp.com/">
    <img class="img-fluid" src="CREATIVE_logo.png"  width="220px" alt="CREATIVE Logo">
  </a>
</p>

<p align="center" style="display: flex; justify-content: center; align-items: center;">
  <a href="https://mediaproject.wesleyan.edu/">
    <img src="wmp-logo.png" width="218px" height="100px" alt="Wesleyan Media Project logo">
  </a>
</p>

<p align="center" style="display: flex; justify-content: center; align-items: center;">
  <a href="https://privacytechlab.org/" style="margin-right: 20px;">
    <img src="./plt_logo.png" width="200px" alt="privacy-tech-lab logo">
  </a>
</p>
