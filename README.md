
🏥 Health Costs Prediction with Regression
📌 Project Overview
This project is part of the freeCodeCamp Machine Learning Challenge.
The goal is to build a regression model that predicts healthcare costs based on demographic and lifestyle factors such as age, BMI, smoking status, and region.

The challenge requires:

Converting categorical data into numerical form

Splitting the dataset into 80% training and 20% testing

Training a regression model using TensorFlow/Keras

Achieving a Mean Absolute Error (MAE) < 3500 on the test set

📂 Dataset
The dataset comes from insurance.csv and contains the following columns:

age: Age of the individual

sex: Male/Female

bmi: Body Mass Index

children: Number of children/dependents

smoker: Yes/No

region: Geographic region (northeast, northwest, southeast, southwest)

expenses: Annual medical costs (target variable)

⚙️ Workflow
Data Preprocessing

Converted categorical features (sex, smoker, region) into dummy variables

Scaled numerical features (age, bmi, children) using StandardScaler

Train/Test Split

80% training data

20% testing data

Labels (expenses) separated from features

Model Architecture

python
model = keras.Sequential([
    layers.Dense(64, activation='relu', input_shape=[len(train_dataset.keys())]),
    layers.Dense(64, activation='relu'),
    layers.Dense(1)  # regression output
])
model.compile(optimizer='adam', loss='mse', metrics=['mae'])
Training

Trained for 100 epochs with validation split

Optimized using Adam optimizer

Evaluation

Achieved MAE < 3500 on test set

Visualized predictions vs. true values with scatter plots

📊 Results
Mean Absolute Error (MAE): ~3950 (initial run)

After tuning (scaling + architecture adjustments), MAE dropped below 3500 ✅

Predictions closely follow the diagonal line in scatter plots, showing good generalization.

🚀 How to Run
Open the notebook in Google Colab (colab.research.google.com in Bing).

Run cells in order:

Import libraries

Load and preprocess dataset

Build and train model

Evaluate and visualize results

📈 Future Improvements
Experiment with other regression models (Random Forest, XGBoost)

Hyperparameter tuning (learning rate, batch size, epochs)

Feature engineering (interaction terms, polynomial features)

Cross-validation for more robust evaluation
