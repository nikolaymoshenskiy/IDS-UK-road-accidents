# From Data to Insights: A Comprehensive Analysis of Traffic Accident Data in the UK (2000-2022)
Authors: Louise Malm & Nikolay Moshenskiy

### Purpose and goal of the project
In the UK, road accidents are responsible for several hundreds of deaths annually, and tens of thousands of severe injuries. This project revolves around the analysis of UK road accident data from 2000 to 2022 and aims to uncover patterns, trends, and factors contributing to road accidents, especially those leading to fatal outcomes. In addition to analysis, a tool classifying an accident as fatal or non-fatal is expected to provide additional insights into the most significant features contributing to fatal accidents. If successful, the classification model could also be used to determine the fatality of simulated situations. Individuals (pedestrians and drivers) might benefit from the results of this project, as it would allow them to plan their routes accordingly.<br>
Therefore, the goals of this project are to (1) identify the most significant predictors of accident fatality, and (2) understand the relationship between various factors and accident outcomes. The first is achieved by training a classifier and extracting the feature importance from it, while the second is achieved by exploratory data analysis of the extracted features among others.

### How to navigate the repository
The repository is structured of subfolders, described in more detail below.<br>
**0_data:** contains processed data files, e.g., train, validation, and test data for machine learning. The original data files are too large to be stored in this repository but can be downloaded from https://www.data.gov.uk/dataset/cb7ae6f0-4be6-4935-9277-47e5ce24a11f/road-safety-data (‘Road Safety Data - Casualties 1979 – Latest Published Year’, ‘Road Safety Data – Vehicles 1979 – Latest Published Year’, and ‘Road Safety Data – Collisions 1979 – Latest Published Year’, as well as ‘Road Safety Open Data Guide – 2023’ for metadata). The data files for this project were downloaded in November 2023, and contain data spanning from 1979 to 2022, however, the original data is likely updated yearly and might contain more years depending on when it is downloaded. <br>
**1_data_preprocessing:** contains Python code (as Jupyter notebooks) for the pre-processing of data; ‘data_preprocessing.ipynb’ for general data pre-processing and ‘preprocessing_ML.ipynb’ for the processing of data for subsequent machine learning (ML). These files are made to be run in the order they are written. The ‘data_preprocessing’ file contains the steps required to recreate visualisations, while the ‘preprocessing_ML’ file contains the necessary steps to obtain machine learning-ready training, validation, and test data sets. The machine learning-ready files can also be obtained from the 0_data folder.<br>
**2_data_visualisations:** contains the Python codes for the visualisations. *A bit more here of how these should be/could be run…* <br>
**3_ML:** contains Python code for training the classifier. *I will add more details about this* <br>
**4_other:** contains other files for the project, for example, the template for the poster, the final poster, etc. <br>
**5_crisp_dm:** contains the Python code and report for business and data understanding according to CRISP-DM principles. The report also contains the project plan. Essentially, a folder containing the information for homework 10 in the Introduction to Data Science course at the University of Tartu, fall 2023.

### Prerequisites
- Download the required data from https://www.data.gov.uk/dataset/cb7ae6f0-4be6-4935-9277-47e5ce24a11f/road-safety-data
- Make sure to have Git LFS (large file storage) installed in case of cloning the repository (to obtain the ML-ready .csv files)
### Dependencies
- Python v 3.8 or newer
- Libraries: numpy, pandas, sklearn, imblearn, plotnine, geopandas, shapely, folium (do we need version numbers?)

### How to use the code
- Make sure that the prerequisites and dependencies are fulfilled.
- Clone the repository or download the Jupyter notebooks of interest. 
- Run the code in a Jupyter Notebook-compatible Python interpreter (e.g., VS Code, Google Colab, Jupyter Notebook). Start by running the notebooks from 1_data_preprocessing, then the other notebooks can be run in any order. Within each notebook, the code should be run in the order it is written (make sure to adjust the paths in the code to work on your machine).
