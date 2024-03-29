# Improved-SENN

-----------------------

## Requirements
  Install the environment using Anaconda with attached environment file as follows.
  
    conda env create -f env.yml

-----------------------

## Data Downloads (Must be done at first)
  Since the pytorch built-in links for downloading the MNIST and the FashionsMNIST dataset are broken, you should download the dataset from the following link:
  
  https://drive.google.com/file/d/1FTF8auc3-TiwO0z3BNw-WDtshBvR0Q8U/view
  
  Download the above .zip file and extract it. This .zip file contains two folders 'MNIST' and 'FMNIST'.
  Move these two folders to the 'data' folder.
  
-----------------------
## Description

Each folder contains the corresponding named experiment.

For example, in the 'Improved-SENN-FMNIST' folder, you can find the codes for the experiments on the Improved-SENN on the FashionMNIST dataset.

For example, in the 'SENN-MNIST' folder, you can find the codes for the experiments on the vanilla SENN on the MNIST dataset.

### List of folders:
  * Improved-SENN-FMNIST : Improved-SENN on the FashionMNIST dataset
  * Improved-SENN-MNIST : Improved-SENN on the MNIST dataset
  * SENN-FMNIST : Vanilla SENN on the FashionMNIST dataset
  * SENN-MNIST : Vanilla SENN on the MNIST dataset
  * VGG-SENN-MNIST : Vanilla SENN on the MNIST dataset with the replacement of the relevance parametrizer to the deeper network VGG8
  * KL-comparison : Improved-SENN on the MNIST dataset with the replacement of the Wasserstein version of the total correlation to the original Kullback-Leibler version of the total correlation.


### 1. SENN-FMNIST and SENN-MNIST
 For the folders 'SENN-FMNIST' and 'SENN-MNIST', there are mainly two ipynb files; one is for training and the other is for evaluation on the trained models.

   #### Train
   * You can train 'SENN-ELU' on the ipynb file named 'Train_Naive.ipynb'.
     * Loss plots are saved in the directory 'TC_naive'
     * The best pre-trained model is saved in the directory 'save_TC_naive'
   * You can train 'SENN-ReLU' on the ipynb file named 'Train_Naive-relu.ipynb'.
     * Loss histories are saved in the directory 'TC_naive_relu'
     * The best pre-trained model is saved in the directory 'save_TC_naive_relu'.

   #### Evaluate
   * You evaluate the results on the trained models using the ipynb file named 'Analyze_Naive.ipynb'.

### 2. Improved-SENN-FMNIST and Improved-SENN-MNIST
For the folders 'Improved-SENN-FMNIST' and 'Improved-SENN-MNIST', there are also mainly two ipynb files; one is for training and the other is for evaluation on the trained models.

   #### Train
   * You can train 'Improved-SENN' on the ipynb file named 'Train_Whole.ipynb'.
     * Loss histories are saved in the directory 'TC'
     * The best pre-trained model is saved in the directory 'save_TC'
   
   #### Evaluate
   * You evaluate the results on the trained models using the ipynb file named 'Analyze.ipynb'.

### 3. KL-comparison
For the folder 'KL-comparison', there are also mainly two ipynb files; one is for training and the other is for evaluation on the trained models.

   #### Train
   * You can train Improved-SENN with the replacement of the Wasserstein version of the total correlation to the original Kullback-Leibler version of the total correlation on the ipynb file named 'Train_Whole.ipynb'.
     * Loss histories are saved in the directory 'TC'
     * The best pre-trained model is saved in the directory 'save_TC'
     
   #### Evaluate
   * You evaluate the results on the trained models using the ipynb file named 'Analyze.ipynb'.
   
### 4. VGG-SENN-MNIST
For the folder 'VGG-SENN-MNIST', there are also mainly two ipynb files; one is for training and the other is for evaluation on the trained models.

   #### Train
   * You can train SENN-ReLU with the replacement of the relevance parametrizer to the deeper network VGG8 on the ipynb file named 'Train_Naive-relu.ipynb'.
     * Loss histories are saved in the directory 'vgg'
     * The best pre-trained model is saved in the directory 'save_vgg'
     
   #### Evaluate
   * You evaluate the results on the trained models using the ipynb file named 'Analyze_Naive.ipynb'.
---------

## Overall Code Structure

There is a folder named 'SENN' in folder for experiments, which is mainly composed of 5 main .py files:

  * aggregator.py - defined the Aggregation functions
  * autoencoder.py - defines the functions that encode inputs into concepts
  * theta_parametrizer.py - defines the functions that generate parameters from inputs (theta(x))
  * discriminator.py - defines the critic function
  * trainer.py - objectives, losses and training utilities for the Improved-SENN
  * trainer_naive.py - objectives, losses and training utilities for the vanilla SENN
  * analyzer.py - evaluation utilities
