# EEG Data Classification with kNN

This project analyzes EEG data from the BONN epilepsy dataset to classify signals into predefined categories using a k-Nearest Neighbors (kNN) classifier. Afterwards it uses a Conditional GAN (cGAN) to generate new data that is also classified by the kNN.

## Project Overview
The goal is to classify EEG signals into three categories:
- *Safe (O)*: Normal signals.
- *Boundary (S)*: Signals at the boundary of abnormality.
- *Unknown (F)*: Signals of uncertain classification.

The kNN model is trained on O and S categories and used to classify F samples.

## Features
The project extracts the following statistical features from the EEG data:
1. *Variance*: Measures the the spread between numbers in a data set. .
2. *Kurtosis*: Used to describe the distribution of the data around the mean.
3. *Entropy*: Quantifies the degree of disorder or uncertainty in the data.

## Dataset
The [BONN epilepsy dataset] is used, which contains EEG signals categorized into different states. 

### Directory Structure:
- O: Safe samples.
- S: Boundary samples.
- F: Unknown samples.

The cGAN architecture creates new samples of each class. Its performance is verified by the kNN.

## Dependencies
The following Python libraries are required:
- numpy
- scikit-learn

Install the dependencies using:
```bash
pip install numpy scikit-learn

Usage

	1.	Extract the BONN epilepsy dataset into the appropriate directory.
	2.	Run the Jupyter Notebook to:
	•	Load and preprocess the dataset.
	•	Train the kNN classifier on O and S samples.
	•	Classify the F samples.

Key Code Components:

	•	Data Loading: Reads EEG signal data and labels from the dataset.
	•	Feature Extraction: Converts raw signals into feature vectors.
	•	kNN Training: Trains a classifier on labeled data.
	•	Prediction: Classifies unknown signals based on the trained model.

Results

The notebook outputs the classifications of the F samples, categorizing them as either safe, boundary, or noise.

