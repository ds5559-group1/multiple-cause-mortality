# multiple-cause-mortality
Pyspark analysis of CDC's multiple cause mortality data

This project was completed as part of UVA's Big Data Analytics course (Fall 2020) and focuses on using PySpark to explore and anylyze CDC Multiple Cause Mortality Statistics (data source: https://www.cdc.gov/nchs/data_access/vitalstatsonline.htm#Mortality_Multiple).

The repository includes the following files:

- Parsing.ipynb: A jupyter notebook which reads in raw txt. files from 2014-2018, slices records into strings based on tape location, and converts into dataframes.
- SparkInit: A jupyter notebook which preprocesses mortality records, creates a stratified sample of ~2.7M records, and splits (80/20) into training and test sets.
- Mortality_EDA: A jupyter notebook that explores the training data with some basic visualizations.
- MCOD_clustering_clean.ipynb: A jupyter notebook that further explores the training data by creating a k-means cluster model using the first 3 causes of death listed.
- Classification_Models.ipynb: A jupyter notebook that fits decision tree, random forest, naive bayes, and MLR models to predict 1st listed cause of death using age, race, marital status, education, sex.
- Classification_Models_DS.ipynb: A jupyter notebook that fits decision tree, random forest, naive bayes, and MLR models to predict 1st listed cause of death using age, race, marital status, education, sex. This training data is downsampled. 
- secondary_cause_final.ipynb: A jupyter notebook that develops a multinomial logistic regression model to predict 2st listed cause of death using age, race, education, and 1st listed cause of death.
- MCOD_clustering.ipynb: A jupyter notebook that develops a K-means clustering model for the first three causes of death. 
- clustering_analysis.ipynb: A jupyter notebook in which the clusters created in MCOD_clustering.ipynb are analyzed. 


Project Status: Completed
