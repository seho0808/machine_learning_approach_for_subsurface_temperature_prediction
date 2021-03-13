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


## Prerequisite Datasets (You have to download these first)
1. AASG Dataset - This file is used throughout the codes and contains the well data throughout North-Eastern USA.
=> Go to https://gdr.openei.org/submissions/638 
=> Click Download next to ThermalQualityAnalysisThermalModelDataFilesStateWellTemperatureDatabases.zip
=> If you unzip, there should be AASG_Thermed_AllThicksAndConds.xlsx

2. Well Dataset - This file is cleaned-up version of new well data (2016~) and used in some of the files.
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

Figure 11 - 0306_Comparing Well Prediction.ipynb

Figure 12 - 0316_Q_map.ipnyb

