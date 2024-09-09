---
title: "Data Analytics Lifecycle Phases"
date: 2024-09-04T00:00:00-08:00
draft: false
tags:
    [
        "Data Analytics",
        "Data Science",
        "Data Engineering",
        "Data Analytics Lifecycle"
    ]
categories: ["Data Science"]
---

This will be a deeper dive into the different phases of the data analytics lifecycle and serves as a continuation for the Data Analytics Lifecycle Overview. 

[Data Analytics Lifecycle Overview](/notes/posts/data-analytics-lifecycle-overview)
<!-- [Data Analytics Lifecycle Overview](/data-analytics-lifecycle-overview.md) -->

## Stages of the Data Analytics Lifecycle
![Data Analytics Lifecycle](/notes/attachments/images/data-analytics-lifecycle.jpeg)
1. **Business Understanding** (Discovery)
2. **Data Acquisition** (Collection)
3. **Data Cleaning** (Preparation)
4. **Data Exploration** (Exploratory Data Analysis)
5. **Predictive Modeling** (Data Modeling)
6. **Data Mining** (Machine Learning)
7. **Data Reporting & Visualization** (Representation & Communication)

---

## Business Understanding
This phases involves gaining a business understanding of the problem or mission objective. Analysts will define major questions of interest, the needs of stakeholders, resources, and constraints.  

## Data Acquisition
This is the phases where the data is collected from various sources. Data can come from either internal data sources such as databases or via external sources such as APIs or web scraping. Analyst will typically use SQL to query and store data in a structured format. 

## Data Cleaning
Once the data has been acquired, data will need to be cleaned and prepared to ensure a high level od data quality. This involves fixing improperly formatted values, dealing with duplicates, missing data, and outliers. Data cleaning is essential to ensure the accuracy of the analysis and skipping this step can result in faulty perceptions of the data. This step can be done with tools such as Python, R, or SQL.

## Data Exploration
Analysts will explore the data to gain a better understanding of the data and its relationships. Exploratory data analysis (EDA) is used to discover patterns, identify basic correlations between variables, and summarize the main characteristics of the data. Sometimes, data visualization tools such as Tableau are used to create insightful graphs that showcase trends and forecasts.

## Predictive Modeling
Analysts will then build predictive models to estimate or project future outcomes. Python and R are used to help automate and the training and use of these models. 

## Data Mining
Data mining is the process of using machine learning algorithms to identify patterns in the data. This can include supervised and unsupervised models, clustering, and classification. Analysts will create training and testing datasets to build models from and determine if groups exist in the data.

## Data Reporting & Visualization
Analysts will tell a story with the data using graphs or interactive dashboards to present the data to other analysts or key stakeholders providing insights and summaries of the analysis. These insights and summaries can provide actionable insights and drive business decisions.

---

## Quick Reference Table

| Phase of Life Cycle | Other Names | Topics of Interest | Potential Problems|
| --- | --- | --- | --- |
| Business Understanding | -Planing <br>-Discovery | -Scope project<br>-Identify stakeholders and research questions/key performance indicators (KPIs)<br>-Identify timeline, budget, and participants | -Lack of clear focus on stakeholders, timeline, limitations, or budget could potentially derail an analysis. |
| Data Acquisition |-Extraction<br>-Data Gathering<br>-Data Query<br>-Data Collection<br>-ETL(Extract, Transform, Load)<br>-WebScraping | -Gather/collect data from a variety of sources<br>-Provide structure to data accessible via relational databases (SQL)<br>-Build data pipeline (ETL)<br>-Use of API to download data from an external source | -Quality and type of data may make access more difficult. |
| Data Cleaning |-Wrangling<br>-Scrubbing<br>-Munging | -Fixing improperly formatted values<br>-Deal with duplicates, missing data, and outliers<br>-Reduce data | -Some cleaning techniques could dramatically change data/outcomes.<br>-Outliers not dealt with can cause problems with statistical models due to excessive variability. |
| Data Exploration |-Exploratory data analysis (EDA)<br>-Descriptive statistics | -Central tendency/measures of center (e.g., mean, median, mode), variability (e.g., standard deviations and quartiles), and distributions (e.g., normal, skewed)<br>-Identify basic correlations between variables<br>-Discover pattern | -Skipping this step could enable faulty perceptions of the data, which hurt advanced analytics. |
| Predictive Modeling |-Data modeling<br>-Correlation-based models<br>-Regression models<br>-Time series |-Estimate/ project future values or likelihood of an event<br>-Extend correlations found in EDA to mathematical models<br>-Predict/ determine output values based on input values<br>-Cross-validate predictive models to ensure accuracy | -Too many input variables (predictors) can cause problems.<br>-Correlation does not imply causation.<br>-Time series models often need sufficient time data to offer precise trending.<br>-Predictive model accuracy should be assessed using cross-validation. |
| Data Mining |-Machine Learning<br>-Deep Learning<br>-Ai(Artificial Intelligence)<br>-Supervised/ unsupervised models<br> | -Create training and testing datasets to build models from<br>-Identify/ detect patterns<br>-Determine if groups (clusters) exist in the data<br>-Classify data into groups<br>-Create models that "learn" and improve (e.g., machine/deep learning, AI) | -Running on entire data is problematic; need to subset data into training and testing datasets to build models. |
| Reporting & Visualization | -Dashboards |-Tell a story with data<br>-Provide a summary of analytics analysis<br>-Provide insights to stakeholders<br>-Create insightful graphs that showcase trends and forecasts | -Due to potential large audience consumption, mistakes can cause bad business decisions and loss of revenue.<br>-Improper scales used in graphs could push for inaccurate interpretations of the story. |

_Source: Table sourced from WGU Data Analytics Program_

