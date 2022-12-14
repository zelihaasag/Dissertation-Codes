# Code Files for Dissertation

This repo consists of the models, utility_functions and all necessary notebooks for each model to run the models in the thesis.

To run this code, you will need to install: NumPy, sklearn, matplotlib, spikeextractors, spiketoolkit, spikesorters, spikewidgets, spikecomparison, MEArec, torch, torchvision, h5py, fastprogress, argparse, warnings, pandas. All the code is based on python 3.

The helpful files for the code:

* **models** file includes the exponential decay and monopolar model for running exponential decay-VAE and monopolar-VAE.
* **utility_functions** file is used for data augmentation and visualizations of the results for exponential decay-VAE and monopolar-VAE.

The following notebooks are required for each model:

* **COM-Monopolar New.ipynb:**  This notebook includes the implementation of COM and Monopolar Triangulation methods using the Spikeinterface library. In this file, an extracellular simulated recording generated by MEArec is used as data. When the correct paths are given for data and saving the outputs, the detected spikes are localized together with the preprocessing, model, and evaluation steps.

There are three main steps required to run the exponential decay-VAE and monopolar-VAE methods.

* **Exponential - VAE_Preprocessing.ipynb and VAE+Monopolar Preprocessing.ipynb:** These jupyter notebooks prepare the data for the model after providing the data and saving paths. After applying the necessary preprocessing steps and data augmentation for this, it creates the h5py file containing the features to be used in the model.

* **Exponential - VAE_Model.ipynb:** This file contains how the model can be trained using VAE. It infers location predictions with the exponential decay model using the dataset.

* **VAE+Monopolar Model.ipynb:** This file contains how the model can be trained using VAE. It infers location predictions with the monopolar model using the dataset.

* **VAE+Monopolar_Preprocessing.ipynb and Monopolar + VAE evaluation.ipynb:** These jupyter notebooks examine how to evaluate the estimated locations with ground truth. It reports the results by applying some evaluation tests to the model results.


