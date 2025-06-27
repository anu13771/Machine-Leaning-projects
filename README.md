🪨 Mine vs Rock Prediction using Logistic Regression

This project uses machine learning to classify sonar signals as either a rock or a mine. The dataset is analyzed, preprocessed, and used to train a Logistic Regression model, which can then predict the object type based on input features.

📂 Dataset
Name: Sonar Dataset

Source: UCI Machine Learning Repository

Format: CSV with 60 numeric features and 1 categorical label (R for Rock, M for Mine)

Each row represents sonar signal returns bounced off a metal cylinder (mine) or a rock in the sea.

🔍 Workflow Summary
1. Importing Dependencies
Used libraries:

pandas, numpy for data handling

scikit-learn for model training, evaluation, and prediction

2. Data Exploration & Processing
Loaded using:

python
Copy
Edit
sonar_data = pd.read_csv('/content/sonar data.csv', header=None)
Performed:

Dataset inspection (shape, describe)

Class distribution: R vs M

Group-wise mean values for basic insight

Split features and labels:

python
Copy
Edit
X = sonar_data.drop(columns=60, axis=1)
Y = sonar_data[60]
3. Train-Test Split
Split 90% training, 10% testing using:

python
Copy
Edit
train_test_split(..., stratify=Y, random_state=1)
4. Model Training
Model Used: Logistic Regression

Trained using:

python
Copy
Edit
model.fit(X_train, Y_train)
5. Evaluation
Accuracy on training data

Accuracy on test data using accuracy_score

6. Prediction System
Accepts new input values

Converts them to NumPy arrays, reshapes, and predicts

Outputs:

Rock if class = R

Mine if class = M

Example:

python
Copy
Edit
input_data = (0.01, 0.0171, ..., 0.0117)
✅ Accuracy Scores
Training Accuracy: 83%

Test Accuracy: 76%

(Values depend on the data split)

🛠 Requirements
Python 3.x

Libraries:

numpy

pandas

scikit-learn

💡 Use Case
This project is ideal for:

Beginners learning ML with real-world datasets

Demonstrating binary classification with basic preprocessing

Practicing model deployment logic (input → predict → interpret)

📁 File
sonar_mine_prediction.ipynb: Complete notebook with data loading, processing, training, and prediction.

🙋‍♀️ Author
Anushka Gupta
Feel free to fork, improve, or reach out for suggestions!
