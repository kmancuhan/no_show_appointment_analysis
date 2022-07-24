# Date Created

July 24, 2022

# Project: No Show Appointment Analysis

## Objective

In this project, my objective is to answer the following questions from a Kaggle dataset about doctor appointments. The dataset has a high no show appointment rate, approximately 30%. Therefore, the following questions make sense for investigation.

  1. What are the characteristics of patients who don't show up to their appointment?
  2. Would the day and month of the scheduled appointment reflect on the no show?
  3. Would scheduling the appointment way more ahead than the actual appointment be related to more no show?

The dataset can be downloaded from here:

https://www.kaggle.com/datasets/joniarroba/noshowappointments

I won't detail here the feature names. The data dictionary in the above page explains well all the 14 features in the dataset.

## Description

The existing Jupyter notebook file shows my general coding style about tackling a data investigation in Python. The code is commented in pretty much most parts. It also shows a template for tacking similar problems for Junior Data Scientists. Data Wrangling section could be organized differently, something that I mentioned in a different repo.

## Main Findings

During my investigation to respond my questions, it turned out that there are quite a lot of records which have wrong date information about the appointment day and the scheduling day. Most of the records actually had the appointment day before the scheduling day which should be the opposite. You can't schedule an appointment after the actual appointment day! After the removal of the erroneous records, the no show appointment turn out to be approximately 5% of all the appointments which make more sense.

Some general trends to answer the questions are:

  1. Patients who don't show up to their appointments tend to be younger. They tend to be more on social welfare, have less hypertension and diabetes; and, have more alcoholism and handicap. When the former 5 factors are analyzed with respect to age, there were some paradoxical observations.
  2. No show appointments tend to increase towards Friday, in general. May has the highest no show rate.
  3. There is not much difference in no show rate for scheduled appointments in advance.

Please check the Jupyter notebook for more detail.

# Files

  - no_show_appointment_analysis.ipynb includes the source code for all the scripts
  - .gitignore basically ignores the data file. It can already be downloaded from the Kaggle page, so I excluded it from here.

# Running Instructions

As long as you have the Jupyter Notebook with a python kernel and the necessary libraries, you should be able to download the code and run the scripts on your local. I am using an Anaconda virtual environment; however, it isn't necessary.

# Requirements
  - conda==4.12.0 (optional)
  - jupyter notebook==6.4.11
  - python==3.9.12
  - pandas==1.4.2
  - numpy==1.21.5
  - matplotlib==3.5.1
