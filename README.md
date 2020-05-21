## ACSE 4.4 - Machine Learning Miniproject
## The Identification Game
#### Team Sigmoid: Hanchao Chen, Mia Chen, Reece Situ, Nicolas Trinephi, Ke Wen

This repository contains two Jupyter Notebooks for the final two submissions to [The Identification Game Kaggle competition](https://www.kaggle.com/c/acse-miniproject/overview) by Team Sigmoid, as part of the ACSE-4 2019/20 module.

### User Instructions & Requirements

The software dependencies can be found in the `requirements.txt` file in this repository. We recommend having at least 12GB of available GPU RAM available when running the notebooks.

The most straightforward way to run the notebooks is via Google Colab. Simply open [Google Colab](https://colab.research.google.com/), log into or create a Google account, select `File > Open notebook > GitHub` and paste the URL of this repository to load the notebooks. Then, select `Runtime > Change runtime type` and change the hardware accelerator to GPU. Once loaded, all cells can be run in order. The notebook will download the dataset used in this project. These notebooks are very memory-heavy in exchange for performance, but the standard allocated 12GB from Colab should be more than enough.

If run locally, we recommend using Conda. Please set up PyTorch by running the following commands:
```
conda create -n torch-env
conda activate torch-env
conda install -c pytorch pytorch torchvision cudatoolkit=10
```
Then navigate to the directory containing the contents of this repository and run the following command to install the rest of the dependencies:
```
conda install --file requirements.txt
```
And run the following to open the notebooks.
```
jupyter notebook
```
Once opened, run all the cells. The notebook will download the dataset used in this project. 

### Documentation

Please refer to `Documentation.txt` for the full documentation of classes and functions defined in the code.

### Dataset

A dataset of 100000 JPEG images (mostly RGB) of dimension 64 x 64 belonging to 200 classes was provided as the training set for this project. A separate set of 10000 JPEG images of the same dimension was provided as the test set. Refer to https://www.kaggle.com/c/acse-miniproject/overview for more information. 



