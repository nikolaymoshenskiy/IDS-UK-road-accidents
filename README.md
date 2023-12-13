# From Data to Insights: A Comprehensive Analysis of Traffic Accident Data in the UK (2000-2022)
Authors: Louise Malm & Nikolay Moshenskiy

## Purpose and goal of the project
In the UK, road accidents are responsible for several hundreds of deaths annually, and tens of thousands of severe injuries. This project revolves around the analysis of UK road accident data from 2000 to 2022 and aims to uncover patterns, trends, and factors contributing to road accidents, especially those leading to fatal outcomes. In addition to analysis, a tool classifying an accident as fatal or non-fatal is expected to provide additional insights into the most significant features contributing to fatal accidents. If successful, the classification model could also be used to determine the fatality of simulated situations. Individuals (pedestrians and drivers) might benefit from the results of this project, as it would allow them to plan their routes accordingly.</br>
Therefore, the goals of this project are to **(1)** identify the most significant predictors of accident fatality, and **(2)** understand the relationship between various factors and accident outcomes. The first is achieved by training a classifier and extracting the feature importance from it, while the second is achieved by exploratory data analysis of the extracted features among others.

## How to navigate the repository
The repository is structured of subfolders, described in more detail below.
#### 00_data
Contains all datafiles used for this project, and processed data files, e.g., train, validation, and test data for machine learning. The original data files were downloaded from https://www.data.gov.uk/dataset/cb7ae6f0-4be6-4935-9277-47e5ce24a11f/road-safety-data (‘Road Safety Data - Casualties 1979 – Latest Published Year’, ‘Road Safety Data – Vehicles 1979 – Latest Published Year’, and ‘Road Safety Data – Collisions 1979 – Latest Published Year’, as well as ‘Road Safety Open Data Guide – 2023’ for metadata). The data files for this project were downloaded in November 2023, and contain data spanning from 1979 to 2022, however, the original data is likely updated yearly and might contain more years depending on when it is downloaded. 
#### 01_data_preprocessing
Contains Python code (as Jupyter notebooks) for the processing of data for subsequent machine learning (ML) (preprocessing_ML.ipynb). The file is made to be run in the order it is written. The file contains the necessary steps to obtain machine learning-ready training, validation, and test data sets. The machine learning-ready files can also be obtained from the 00_data folder.
#### 02_data_analysis_visualisation
Contains the Python codes for the analysis and visualisations of the data. It contains three files, one with temporal analysis of the data (temporal_analysis.ipynb), one with spatial analysis of the data (spatial_analysis.ipynb) and one with accident severity analysis (accident_severity.ipynb). These can be run in any order one wishes.
#### 03_ML
Contains Python code for training the classifiers (ML_classifiers.ipynb) with some comments and evaluations. It needs to be run in the order it is written. The best performing model was also tested on an unused test set of the data.
#### 04_other
Contains other files for the project: the poster and initial data exploration python code (exploration_collisions.ipynb and exploration_collisions_vehicles.ipynb). These files are optional.
#### 05_crisp_dm
Contains the Python code and report for business and data understanding according to CRISP-DM principles. The report also contains the project plan. Essentially, a folder containing the information for homework 10 in the Introduction to Data Science course at the University of Tartu, fall 2023.

## Prerequisites
- Make sure to have Git LFS (large file storage) installed in case of cloning the repository (to obtain all data files).

## Dependencies
- Python 3
- Libraries: numpy, pandas, scikit-learn, imbalanced-learn, joblib, plotnine, seaborn, matplotlib, geopandas, shapely, folium.
One option is to create a virtual environment:
    1. python -m venv myenv
    2. Activate environment and run: pip install -r requirements.txt

## How to use the code
- Make sure that the prerequisites and dependencies are fulfilled.
- Clone the repository or download the Jupyter notebooks of interest. 
- Run the code in a Jupyter Notebook-compatible Python interpreter (e.g., VS Code, Google Colab, Jupyter Notebook). Start by running the notebooks from 01_data_preprocessing, then the other notebooks can be run in any order. Within each notebook, the code should be run in the order it is written.
