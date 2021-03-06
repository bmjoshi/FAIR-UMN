# FAIR-UMN: Identifying Interaction Location in SuperCDMS Detectors



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
└── doc                                   /* Documents for our project.
|
|
└── fair_gpu.yml                          /* The YML file to create a GPU execution environment.
|
|
└── fair_cpu.yml                          /* The YML file to create a CPU execution environment.
|
|
└── LICENSE                               /* The MIT LICENSE.


```


Below, we provide more details about each folder.

- **data**. This folder contains several Jupyter notebooks for preprocessing the dataset and preparing the dataset for use with the neural network models.

- **src**. This folder contains the core code for neural network models, including the model architecture, auxiliary functions, and a Jupyter notebook to train and validate the model.

- **analysis**. This folder contains several Jupyter notebooks that are used to extract the predictions made by the neural network models, format these predictions into a neat csv file, and analyze these predictions (e.g., generating figures and obtaining statistics such as mean and standard deviations of predictions).


## Get Startted

We provided two options for users to set up the execution environment: 
- we provide the envrionment YML file so that one can set up the execution envrionment with it direclty;
- we provide the detailed steps and commands to install each required package. 

### Set up from the YML file

1. Get and clone the github repository:

   `git clone https://github.com/ml-deepai/FAIR-UMN`

2. Switch to `FAIR-UMN` :

   `cd XXX/FAIR-UMN`  (*Note*: `XXX` here indicates the upper directory of `FAIR-UMN`. For example, if you clone `FAIR-UMN` under `/home/Download`, then you should replace `XXX` with `/home/Download`.)

3. Deactivate conda base environment first you are in (otherwise, go to step 4 direclty) (We use [Anaconda3](https://www.anaconda.com/products/individual-d)):

   `conda deactivate`

4. Create a new conda environment with the YML file (choose GPU or CPU version according to your computational resources):

    GPU version run: `conda env create -f fair_gpu.yml`
   
    CPU version run: `conda env create -f fair_cpu.yml`

5.  Activate conda environment:
    
    `conda activate fair_gpu` (If you choose the GPU version in Step4)
    
    `conda activate fair_cpu` (If you choose the CPU version in Step4)

6. You are now ready to explore the codes/models! Please remember to follow this order: *data*->*src*->*analysis*



### Set up from the source

1. Get and clone the github repository:

   `git clone https://github.com/ml-deepai/FAIR-UMN`

2. Switch to `FAIR-UMN` :

   `cd XXX/FAIR-UMN`  (*Note*: `XXX` here indicates the upper directory of `FAIR-UMN`. For example, if you clone `FAIR-UMN` under `/home/Download`, then you should replace `XXX` with `/home/Download`.)

3. Deactivate conda base environment first you are in (otherwise, go to step 4 direclty) (We use [Anaconda3](https://www.anaconda.com/products/individual-d)):

   `conda deactivate`

4. Create a new conda environment:

   `conda create -n fair_umn python=3.6`

5.  Activate conda environment:
    
    `conda activate fair_umn`

6. Install Pytorch (choose GPU or CPU version according to your computational resources):

   GPU version run: `conda install pytorch torchvision torchaudio cudatoolkit=10.2 -c pytorch`
   
   CPU version run: `conda install pytorch torchvision torchaudio cpuonly -c pytorch`
   
7. Install scikit-learn

   `pip install scikit-learn`

8. Install pandas

   `pip install pandas`

9. Install matplotlib

   `pip install matplotlib`
 
10. Install numpy

    `pip install numpy`
 
11. Install seaborn

    `pip install seaborn`
 
12. Install tqdm

    `pip install tqdm`
    
13. Install Jupyter notebook

    `pip install notebook`

14. You are now ready to explore the codes/models! Please remember to follow this order: *data*->*src*->*analysis*

   
*Note*: 
1) To install Anaconda, please follow its [official guideline](https://docs.anaconda.com/anaconda/user-guide/getting-started/).
2) We test our model on Ubuntu 20.04.



## Support or Contact

If you need any help, please feel free to contact us!  

