# Improved-SENN

---

## Dependencies

### Major:

  * python = 3.7.9
  * pytorch = 1.7.1
  
### Minor:
  * tensorflow = 2.3.0
  * tensorboard = 2.4.1
  * numpy
  * matplotlib

---

## Description

Each folder contains the corresponding named experiment.
For example, in the 'Improved-SENN-FMNIST' folder, you can find the codes for the experiments on the Improved-SENN on the FashionMNIST dataset.
For example, in the 'SENN-MNIST' folder, you can find the codes for the experiments on the vanilla SENN on the MNIST dataset.

### SENN-FMNIST and SENN-MNIST
For the folders 'SENN-FMNIST' and 'SENN-MNIST', there are mainly two ipynb files; one is for training and the other is for analysis on the trained models.
  * You can train 'SENN-ELU' on the ipynb file named 'Train_Naive.ipynb'
    * Loss plots are saved in the directory 'TC_naive'
    * The best model is saved in the directory 'save_TC_naive'
  * 

For the folders 'Improved-SENN-FMNIST' and 'Improved-SENN-MNIST', there are also mainly two ipyn files

### List of folders:
  * Improved-SENN-FMNIST : Improved-SENN on the FashionMNIST dataset
  * Improved-SENN-MNIST : Improved-SENN on the MNIST dataset
  * SENN-FMNIST : Vanilla SENN on the FashionMNIST dataset
  * SENN-MNIST : Vanilla SENN on the MNIST dataset
  * VGG-SENN-MNIST : Vanilla SENN on the MNIST dataset with the replacement of the relevance parametrizer to the deep network VGG8
  * KL-comparison : Improved-SENN on the MNIST dataset with the replacement of the Wasserstein version of the total correlation to the original Kullback-Leibler version of the total correlation.
  
