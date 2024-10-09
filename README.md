# Cryptocurrency Price Direction Predictor

This repository contains my solution for the Cryptocurrency Price Direction Predictor competition hosted by ciccada3301 on Kaggle. The goal of this competition is to develop a model that accurately predicts whether the price of a cryptocurrency will move up or stay the same/move down in the next minute, based on historical data.

## Model Selection and Experiments

### 1. Random Forest Classifier

The final model used for prediction is a Random Forest Classifier. Extensive experimentation was conducted to identify the best hyperparameters using GridSearchCV. The following parameters were tuned:

	•	n_estimators: Number of trees in the forest.
	•	max_depth: Maximum depth of the trees to control overfitting.
	•	max_features: Number of features to consider for the best split.

Final Random Forest Model Performance:

	•	F1 Score: 0.76556
	•	Accuracy: The model achieved a relatively strong performance in terms of classification accuracy and F1 score, indicating a good balance between precision and recall.

### 2. LSTM Model

I also experimented with using a Long Short-Term Memory (LSTM) neural network to capture sequential dependencies in the price data, but didn't include it in my final solution due to underfitting. The LSTM model was built with the following architecture:

	•	Architecture:
	•	2 LSTM layers with 128 and 64 units, respectively.
	•	Dropout layers to reduce overfitting.
	•	A Dense layer with a sigmoid activation function for binary classification.
	•	Features: The LSTM model used a similar set of technical indicators, along with lagged features to provide a sequence of historical data
