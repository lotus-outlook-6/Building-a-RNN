# Building-a-RNN

[Open in Colab](https://colab.research.google.com/github/lotus-outlook-6/Building-a-RNN/blob/main/rnn.ipynb) • Jupyter Notebook tutorial for building an LSTM-based Recurrent Neural Network to predict Google stock prices.

## Overview
This repository contains a hands-on Jupyter Notebook (rnn.ipynb) that walks through preprocessing, building, training, and evaluating an RNN (stacked LSTM) for time-series stock-price prediction using Keras/TensorFlow. It demonstrates a practical workflow: feature scaling, creating timesteps, building a multi-layer LSTM with Dropout, training, and visualizing predicted vs. real stock prices.

## Contents
- rnn.ipynb — The full tutorial and runnable notebook:
  - Data preprocessing (MinMax scaling, 60-timestep windows)
  - Model: 4 LSTM layers (50 units each) with Dropout(0.2), Dense output
  - Training: compiled with Adam, mean squared error loss; default in-notebook run uses 100 epochs, batch size 32
  - Prediction and visualization of Google stock prices for 2017

## Datasets
The notebook expects the CSV files:
- `Google_Stock_Price_Train.csv`
- `Google_Stock_Price_Test.csv`

These CSV files are not included in the repository. Place them in the repository root (or update file paths in the notebook) before running locally, or upload them to Colab when prompted. The notebook expects the `Open` column to be available and uses it as the target feature.

## Requirements
- Python 3.8+
- Jupyter / Google Colab
- Key Python packages:
  - numpy, pandas, matplotlib
  - scikit-learn
  - tensorflow (or keras with a compatible TF backend)

Install quickly:
