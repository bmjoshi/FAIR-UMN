# FAIR-UMN: Identifying Interaction Location inSuperCDMS Detectors



## Overview

This github repository contains the code for analyzing and modeling the CDMS data. The code is written in Python. In most cases, we provide a Jupyter notebook with inline descriptions while in some cases (e.g., the model and its  auxiliary functions) we provide a Jupyter notebook and python scripts. 

Besides this github repository, we have a complementary document that provides background for this problem, describes the purposes of this project,  and introduces the dataset and neural network models in more details. The document can be [downloaded here](https://github.com/ml-deepai/FAIR-UMN/blob/main/doc/FAIR%20Document%20-%20Identifying%20Interaction%20Location%20in%20SuperCDMS%20Detectors.pdf). 

We also have a project web-page which can be accessed via [this link](https://ml-deepai.github.io/FAIR-UMN/).



This repository includes the following folders and/or files. For *folders*, we provide a respective *Readme* document inside. The structure of folders is shown below: 

```
.
├── data                                  /* All you need to preprocess the dataset.
|   ├── raw_txt                           /* Original dataset in the txt format.
|   ├── processed_csv                     /* Extracted features in the csv format.
|   ├── dnn_dataset                       /* Training/validation/test data for deep neural network models.
|   ├── feature_analysis                  /* Resuts/figures for visualization the distribution of features (before/after normalization).
|   ├── 1_txt2csv.ipynb                   /* Jupyter notebook to extract featrues from original dataset (in the txt format).
|   ├── 2_prepare_dataset.ipynb           /* Jupyter notebook to get training/validation/test dataset.             
|   ├── 3_features_analysis.ipynb         /* Jupyter notebook to visualize the distribution of features (before/after normalization).     
|   └──  README.md 
|
|
├── src                                   /* All you need to train the deep neural network (DNN) models.
|   ├── DNN_Regression                      
|   |   ├── model_files                   /* A folder that hosts the backbone of deep neural network models (e.g., model definition and its auxiliary functions).
|   |   ├── train_deep_regression.ipynb   /* Jupyter notebook to train and test the deep neural network models. 
|   └── README.md 
|
|
├── analysis                              /* All you need to analyze the results generated by the DNN model.
|   ├── hist_results                      /* The histogram of predictions.
|   ├── stat_results                      /* The statistical information of predictions (e.g., the mean and standard deviation).
|   ├── 1_statistical_info.ipynb          /* Jupyter notebook to get the statistical information of predictions.         
|   ├── 2_visualization.ipynb             /* Jupyter notebook to generate the histogram of predictions.   
|   └── README.md  
|
|
└── doc                                   /* documents for our project.

```


Below, we provide more details about each folder.

- **data**. This folder contains several Jupyter notebooks for preprocessing the dataset and preparing the dataset for use with the neural network models.

- **src**. This folder contains the core code for neural network models, including the model architecture, auxiliary functions, and a Jupyter notebook to train and validate the model.

- **analysis**. This folder contains several Jupyter notebooks that are used to extract the predictions made by the neural network models, format these predictions into a neat csv file, and analyze these predictions (e.g., generating figures and obtaining statistics such as mean and standard deviations of predictions).


## Get Startted

1. Get and clone the github repository:

   `git clone https://github.com/taihui/cdms_fair`

2. Switch to `cdms_fair` :

   `cd XXX/cdms_fair`  (*Note*: `XXX` here means the upper directory of `cdms_fair`. For example, if you clone `cdms_fair` under `/home/Download`, then you should replace `XXX` with `/home/Download`.)

3. Deactivate conda base environment first you are in (otherwise, go to step 4 direclty):

   `conda deactivate`

4. Install conda environment:

   `conda env create -f fair.yml`

5.  Activate conda environment:
    
    `conda activate fair`

6. You are now ready to explore the codes! Please remember to follow this order: *Data_Preprocessing*->*DNN_Models*->*Results_Analysis*

   

*Note*: 
1) To install Anaconda, please follow its [official guideline](https://docs.anaconda.com/anaconda/user-guide/getting-started/).
2) We test our model on Ubuntu 20.04.



## Support or Contact

If you need any help, please feel free to contact us!  

