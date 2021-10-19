## What is this README and REPO?
This repository provides python codes to reproduce the plots and tables from 
the paper Exploratory Analysis of Machine Learning Methods in Geothermal Energy Research.
(https://geothermal-energy-journal.springeropen.com/articles/10.1186/s40517-021-00200-4)
The file formats are in Jupyter Notebook IDE format (.ipynb).
If you wish to obtain a .py version, please email to seho0808@vt.edu.

## How to use the repo?

First, there is a video describing how to reproduce the results. Link: https://www.youtube.com/watch?v=lc5TMNuvQ-8&ab_channel=%EC%84%B8%ED%98%B8

To reiterate what the video was talking about,

1. download the AASG Dataset and clean_new_well_data_fixed.csv and optim_result.out files.
2. download any of the .ipynb code files from github that you would like to run.
3. if you want to use the saved model, you should look at the "Load Saved Pickle Models.ipynb" file.

## File Description
### 0305_Compare_New_and_Old_LONG_LAT.ipynb
This file compares the latitude and longitude information of the datasets.

### Figure_11_Comparing_Well_Prediction.ipynb
This file has two legacy files in the repository. This one is the most current one.
In "0310_HPTuning+ExcelMetric+NewWellMetric.ipynb", we tune the hyperparameters of the machine
learning models. In "Final Metrics and Graphs.ipynb", the tuned hyperparameters are actually used
to test for the test data(which are the new well data). In "Figure_11_Comparing_well_prediction.ipynb",
we had to change the models' training and testing process to K-fold which lead us to regenerate the plots and data. 
*The metrics and graphs are listed inside the file as well.

### Figure_12_Q_map.ipynb
Regenerated Q map with retuned XGBoost from the legacy file "0316_Q_map.ipynb".

### Figure_8_depth_maps.ipynb
Regenerated heat maps per depth from the legacy file "0314_depth_maps.ipynb".

### HP_Tuning.ipynb
This file has the code that tunes all the models with appropriate hyperparameters.
Also contains saving the pickle files as .sav files.
The pickle files generated here can be downloaded from here:

finalized_model_RF.sav: https://drive.google.com/file/d/130C3hOhBRKxC-CZ_QTQpTMcQw6RuwCsc/view?usp=sharing

finalized_model_XGB.sav: https://drive.google.com/file/d/1NY8Z-Ukrhz6gS-pkKoW7RuK6Z2_5j2XW/view?usp=sharing

### Saving Pickles for Ridge and Keras.ipnyb
This file is saves Ridge and Keras pickle files.
Result files are available at:

finalized_model_DNN.zip: https://drive.google.com/file/d/1x5wHJkuPohdscIif7Sk1QI_vSmPWyEX8/view?usp=sharing

finalized_model_ridge.sav: https://drive.google.com/file/d/1ZzKDvbT6I2422Rg886c16ZUDyHAATrYd/view?usp=sharing

### fixing_clean_well_data.ipynb
We previously used an incorrect method to correct the new well data. After
a major change in paper, we rectify the wrong method with a correct formula. The
data engineering part of that process is inside this file.

### Table_5_Q_Prediction.ipnyb
Gradient prediction comparison for all models. Used in table 5 of the original paper.

### _Organized Tests.ipynb
This is a legacy version of "0310_HPTuning+ExcelMetric+NewWellMetric.ipynb". 
Only the importance plot matters in this file for use.


## Legacy Files

### 0306_Comparing Well Prediction.ipynb
This file is a legacy file for "Final Metrics and Graphs.ipynb" file. Hence, you can ignore it.
It was kept to show the last version before the major change.

### 0310_HPTuning+ExcelMetric+NewWellMetric.ipynb
Legacy version for "HP_Tuning.ipynb" file. It was kept to show the last version before the major change.

### 0314_depth_maps.ipynb
Comparing algorithms for the interpolation of the heat map. Legacy file for "Figure_8_depth_maps.ipynb".

### 0315_map_excel_data.ipynb
Tuning the KNN interpolation method.

### 0316_Q_map.ipynb
Q map with XGBoost. Legacy file for "Figure_12_Q_map.ipynb".

### Final Metrics and Graphs.ipynb
Legacy file for "Figure_11_Comparing_Well_Prediction.ipynb".

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

Figure 7 - HP_Tuning.ipynb

Figure 8 - Figure_8_depth_maps.ipynb

Figure 11 - Figure_11_Comparing_Well_Prediction.ipynb

Figure 12 - Figure_12_Q_map.ipynb

## Video Link
We also provide a video instruction about how to access data and run the models.
https://youtu.be/4Gp_sEUGNi8

## Tunned Hyper-parameters for all models
Ridge 
  alpha:	10
  
RF
  Max_depth:	10
  n_estimators: 50
  
XGB
  alpha:	1
  lambda:	10
  Max_depth:	10
  n_estimators=100
  gamma:	0.1
  
DNN
  structure	50-50-1
  optimizer	ADAM
  loss	Mean squared error
