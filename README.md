# Solana-Price-Prediction-Model-Using-LSTM
Solana Price Prediction using LSTM: A deep learning project leveraging historical Solana price data from 13/07/2020 to 1/10/2024 to forecast future trends with a Long Short-Term Memory (LSTM) model.

# Project Features
### Data Processing: Cleaned and prepared historical Solana price data for training.
### Feature Engineering: Utilized only essential columns for analysis and applied scaling techniques for efficient model training.
### LSTM Model: Built and trained a multi-layer LSTM model to predict Solana's price.
### Visualization: Plotted the training, validation, and predicted prices for clear performance analysis.

# Key Technologies
1. Python (pandas, numpy, seaborn, matplotlib)
2. Keras/TensorFlow for deep learning
3. Scikit-learn for preprocessing
4. Google Colab for model training

# Dataset
The dataset includes 4 years of daily Solana price data with the following features:

1. Date: Daily timestamps.
2. Price: Close price of Solana (used as the target variable).
3. Other Columns: High, Low, Volume, and Change %, which were dropped during preprocessing.

# Workflow
## Data Cleaning:
1. Removed unnecessary columns.
2. Converted date to datetime format and sorted data in ascending order.
## Feature Scaling:
1. Applied Min-Max Scaling to normalize prices between 0 and 1.
## Data Splitting:
1. Used 80% of the data for training and 20% for testing.
2. Prepared sequences of 60 timesteps to feed into the LSTM.
## Model Design:
1. Stacked LSTMs with:
- Layer 1: 512 units, relu activation, return sequences.
- Layer 2: 256 units, relu activation.
- Dense output layer for predictions.
- Loss Function: Mean Squared Error (MSE).
- Optimizer: Adam.
## Training:
1. Trained the model for 35 epochs with a batch size of 32.
2. Included Mean Absolute Error (MAE) as a metric for evaluation.
## Prediction:
1. Predicted prices for the test set and scaled them back to the original range.
Visualization:
2. Plotted training, validation, and predicted prices for performance evaluation.
   
## Results
The model successfully learned temporal dependencies in the data, achieving competitive performance as indicated by a low Mean Squared Error (MSE) and Mean Absolute Error (MAE) on the validation set.
