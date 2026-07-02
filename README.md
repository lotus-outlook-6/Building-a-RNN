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
## How to run

- Recommended (easiest): Open and run in Google Colab
  1. Click the Colab link at the top of this README or open:
     https://colab.research.google.com/github/lotus-outlook-6/Building-a-RNN/blob/main/rnn.ipynb
  2. Upload the required CSV files to the Colab session (Files pane) or mount Google Drive and update paths.
  3. Run cells sequentially.

- Run locally:
  1. Clone the repo:
     git clone https://github.com/lotus-outlook-6/Building-a-RNN.git
  2. Install dependencies (see Requirements).
  3. Place the CSV files in the repo root.
  4. Start Jupyter and open the notebook:
     jupyter notebook rnn.ipynb
  5. Run cells top-to-bottom.

- Headless execution (execute notebook from command line):

## Model & training notes
- Input window / timesteps: 60
- Architecture: 4 stacked LSTM layers (50 units each), Dropout(0.2) after each LSTM
- Output: single Dense unit (predicted stock price)
- Optimizer: Adam; loss: mean squared error
- Example training hyperparameters used in notebook: epochs = 100, batch_size = 32

## Results / Visualization
The notebook produces a plot comparing the real Google stock price (test) and the model's predicted values, and prints training progress (loss per epoch) in the output.

## Tips & improvements
- Add a requirements.txt with pinned versions for reproducibility.
- Save the trained model (model.save(...)) and include code to load it for inference to avoid retraining every run.
- Consider using callbacks (EarlyStopping, ModelCheckpoint) and parameter tuning for better generalization.
- Provide a link or script to download the example CSVs or include a small sample for quick testing.

## License
No license file included. Add a LICENSE if you want to make usage/redistribution terms explicit.

## Contributing
Open an issue or a pull request to suggest improvements, add datasets, or include a requirements file / saved model.
