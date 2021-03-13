## What is this README and REPO?
This repository provides python codes to reproduce the plots and tables from 
the paper Exploratory Analysis of Machine Learning Methods in Geothermal Energy Research.
The file formats are in Jupyter Notebook IDE format (.ipynb).
If you wish to obtain a .py version, please email to seho0808@vt.edu.

## How to use the repo?

First, there is a video describing how to reproduce the results. Link: ~
To reiterate what the video was talking about,

1. download the AASG Dataset and clean_new_well_data_fixed.csv and optim_result.out files.
2. download any of the .ipynb code files from github that you would like to run.
3. if you want to use the saved model, you should look at the "Load Saved Pickle Models.ipynb" file.

## File Description
### 0305_Compare_New_and_Old_LONG_LAT.ipynb
This file compares the latitude and longitude information of the datasets.

### 0306_Comparing Well Prediction.ipynb
This file is a legacy file for "Final Metrics and Graphs.ipynb" file. Hence, you can ignore it.
It was kept to show the last version before the major change.

### 0310_HPTuning+ExcelMetric+NewWellMetric.ipynb
This file has the code that tunes all the models with appropriate hyperparameters.

### 0314_depth_maps.ipynb
Comparing algorithms for the interpolation of the heat map.

### 0315_map_excel_data.ipynb
Tuning the KNN interpolation method.

### 0316_Q_map.ipynb
Q map with XGBoost

### Final Metrics and Graphs.ipynb
In 0310_HPTuning+ExcelMetric+NewWellMetric.ipynb, we tune the hyperparameters of the machine
learning models. In Final Metrics and Graphs.ipynb, the tuned hyperparameters are actually used
to test for the test data(which are the new well data). Then, the metrics and graphs are listed inside
the file as well.

### Load Saved Pickle Models.ipynb
This file loads the saved pickle xgb model. You need to generate the pkl file first.
There is one that is already generated, xgbSaved.pkl.
The link to download xgbSaved.pkl is, https://drive.google.com/file/d/1XJpMLYp6bk-VFWVAf69CTh3vcDds6OOm/view?usp=sharing.

### Save Pickle File from Models.ipynb
This saves xgb pickle file after training. It doesn't work for dnn as our api
seem to crash when pickle is applied after training process. Hence, only
xgb model is provided as a saved version. You can still generate dnn model in a few minutes
by running our code.

### fixing_clean_well_data.ipynb
We previously used an incorrect method to correct the new well data. After
a major change in paper, we rectify the wrong method with a correct formula. The
data engineering part of that process is inside this file.

### _Organized Tests.ipynb
This is a legacy version of 0310_HPTuning+ExcelMetric+NewWellMetric.ipynb. 
Only the importance plot matters in this file for use.

## Prerequisite Datasets (You have to download these first)
1. AASG Dataset - This file is used throughout the codes and contains the well data throughout North-Eastern USA.
=> Go to https://gdr.openei.org/submissions/638 
=> Click Download next to ThermalQualityAnalysisThermalModelDataFilesStateWellTemperatureDatabases.zip
=> If you unzip, there should be AASG_Thermed_AllThicksAndConds.xlsx

2. New Well Dataset - This file is cleaned-up version of new well data (2016~) and used in some of the files.
=> Go to https://drive.google.com/file/d/1sm0CdmvixpEOpWiGkrh3rTVb7nz0r8pH/view?usp=sharing

## Document Figures
Many of the figures and tables are omitted as they are not produced by ourselves, or
of less importance in terms of code documentation.

Figure 1 - 0305_Compare_New_and_Old_LONG_LAT.ipynb

Figure 6 - _Organized Tests.ipynb*
*This is a legacy version of 0310_HPTuning+ExcelMetric+NewWellMetric.ipynb.
Therefore, you should ignore everyting except the importance plot.

Figure 7 - 0316_Q_map.ipynb

Figure 8 - 0314_depth_maps.ipynb & 0315_map_excel_data.ipynb

Figure 11 - Final Metrics and Graphs.ipynb

Figure 12 - 0316_Q_map.ipnyb

## Video Link
We also provide a video instruction about how to access data and run the models.
https://youtu.be/4Gp_sEUGNi8
