# MAST30034 Project 1 README.md
- Name: Lang (Ron) Chen

**Research Goal:** My research goal is to find the PULocation with the highest demand given a DOLocation at a specific 
time

**Report**
FOR METHOD USED AND RESULTS OF THIS PROJECT PLEASE SEE [`./report/MAST30034_ADS_A1_1181506.pdf`](https://github.com/TGChenZP/MAST30034-A1__Py/blob/main/report/MAST30034_ADS_A1_1181506.pdf)


**Timeline**: The timeline for the research area is 2016 Jan - June

All code used in this research was put in .ipynb format, for better visualisation of partial output compared to `.py` 
scripts. 

Whilst there were some repeated code which were not functionalised, this was done so because each script needed little 
tweaks that would have made any generalisations difficult (i.e., the alternative would have been a significant number 
of if-else conditioning in functions which decreases readability)

Please run in order as listed below to ensure outputs are generated.

Holiday data was manually scraped from website so was committed.
Weather data was committed because an account needs to be created to download and each day is limited to a certain 
amount of free downloads.

Please download files that belong in `./data/raw/NYC_Taxi/taxi zones` from 
`https://github.com/akiratwang/MAST30034_Python` (belongs to source NYC TLC, but recently removed so head tutor made
it available on tutorial repository)

1. `Download Data.ipynb`: downloads data
2. `EDA Part 1.ipynb`: EDA using pandas
3. `EDA Part 2.ipynb`: EDA using spark
4. `Iteratively Clean and Aggregate.ipynb`: drops outliers and aggregates data
5. `Prepare discrete classifier data.ipynb`: adds discrete labels to data
6. `Prepare continuous predictor data.ipynb`: adds continuous labels to data
7. `Discrete Data Fine Preprocessing.ipynb`: outputs final discrete labelled dataset used
8. `Continuous Data Fine Preprocessing.ipynb`: outputs final continuous labelled dataset used
9. `Trial of Train Discrete Model.ipynb`: trials different classifiers at default settings
10. `Trial of Train Discrete Model - Separate.ipynb`: trials (future improvement) of one classifier per DOL
11. `Trial of Train Continuous Model.ipynb`: trials different predictors at default settings
12. `Trial of Train Continuous Model - Separate.ipynb`: trials (future improvement) of one predictor per DOL
13. `Tuning (YZ) Unified Disc RFC Entropy.ipynb`: YangZhou (greedy/heuristic) Class tuning of Random Forest Classifier
14. `Tuning (YZ) Unified Disc RFC Gini.ipynb`: YangZhou Class tuning of Random Forest Classifier (Gini split)
15. `Tuning (JC) Unified Disc LogReg.ipynb`: JiaoCheng (brute force) Class tuning of Logistic Regression
16. `Tuning (YZ) Unified Cont RFR.ipynb`: YangZhou Class tuning of Random Forest Regressor
17. `Tuning (JC) Unified Cont RFR.ipynb`: JiaoCheng Class tuning of Random Forest Regressor
18. `Train Final Model - LogReg.ipynb`: Trains and gathers data for final Logistical Regression model
19. `Train Final Model - RandomForestRegressor.ipynb`: Trains and gathers data for final Random Forest Regression model
20. `Analysing Accuracy and MSE and Creating Maps.ipynb`: Produces Folium maps using data from final model

The tuning section uses a self built heuristical/greedy algorithm called YangZhou. All code for this algorithm can be 
found in `./notebooks/YangZhou`. The files are kept in the `./notebooks` directory because if outside of nested 
directory of notebooks that use it, will have to toggle with sys and PATH - which is complicated and need to be
manually adjusted for each machine that downloads it.

**Information referred to in report**
Tuning results can be found in `./data/curated/tuning`; score data about each zone can be found in 
`./data/curated/final_model_data`; Plots can be found in `./plots`; Statistics referred in report such as number of 
rows dropped, number of rows after aggregation and each clean, F-scores can be found in notebook 3, 4, 5, 6, 7.

