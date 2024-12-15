# <ins>Bio_imaging_data_analysis</ins>
## This respiratory contains scripts generated for analysing image-based tabular data.
### 4 scripts are available - per plate will work on each plate separately, combine plates will combine the plate and then run the analysis and timelapse scripts will work with the same logic but for timelapse data. 
### All scripts take as input a main folder with a file folder in it with txt files - see file examples above. 
### All output files will be saved in the main folder.
### Analysis steps include : 
* Converting txt files to csv files step - including convertion of txt to csv files, adding PC ( plate condition such as 24, 48 hours of regular/starvation medium or any other noted condtion ) and an option to remove wells that were flagged during the experiment. 
* For combine plate scripts, next step will combine these csv files into one data frame. 
* Choosing columns for the analysis step - choosing unwanted column to remove, important feature columns which will be used for the analysis and index columns that will be used for grouping wells ( rows ) from the files. 
* Data processing and main analysis step, this includes -
  - Creating multiple indexes based on the index columns ( all possible combination of indexes )
  - Option to remove values based on different columns, removing specific cell ids based on cell_id and to remove additional columns if needed.
  - Creating statistical summary based on chosen index & removal of rows based on cell count
  - Creating box plots for each feature based on chosen index
  - creating an excel & ppt file for each group ( cell_type, compund, concentartion)
  - Creating a heatmap and pca's based on chosen index.
  - Outlier detection based on chosen index and based on one of four methods - z score, iqr, percintiles or Local outlier factor.
  - Choice of downstreram index columns
  - Feature quality control based on random forest scoring, coefficient of variation and correlations.
  - Option to rename feature names.
  - For timelapse data, timelapse plots will be generated based on chosen index
  - Data imputation and normalization step - includes imputation based on median values and normalization using - z score, min-max, central log, logarithmic scale, box-cox, Q-Q plots and histograms will be genertaed for each method.
  - Choice of normalization method to end analysis. 
* A dashobard will be generated to simplify the examination of results.
  ### Output data is optimized for statistics and final visualzation.



## Refernces : 
- Caicedo et al. Data-analysis strategies for image-based cell profiling.
- Pedregosa et al. Scikit-learn: Machine Learning in Python.
- Virtanen et al. SciPy 1.0: fundamental algorithms for scientific computing in Python.
- Breunig et al. LOF: Identifying Density-Based Local Outliers.
- 

