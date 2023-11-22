# Breast_cancer_predictor
creat an app with streamlit that helps predicting breast cancer using (Breast Cancer Wisconsin (Diagnostic) Data Set)
Streamlit Breast Cancer Prediction App

Welcome to the Streamlit Breast Cancer Prediction App! This application utilizes machine learning to predict whether a breast tumor is malignant
or benign based on the Wisconsin Breast Cancer Dataset.

Dataset Overview

The Wisconsin Breast Cancer Dataset consists of 569 observations with 30 feature variables for model training. 
The last two variables include an ID number and the diagnosis (M = malignant, B = benign). 
The model is trained using the first 30 variables, and the diagnosis variable is used for evaluation.

Data Cleaning and Model Training

Prior to model training, we perform necessary data cleaning steps, such as dropping the ID column and an empty column named Unnamed: 32. 
The diagnosis variable is encoded using the map function from pandas. The Logistic Regression algorithm from sklearn.linear_model is employed for training, 
preceded by data normalization using StandardScaler from sklearn.preprocessing.

To enhance predictive performance, we built an ensemble model using the three most performing models out of five different models.

Testing the Model

To assess the model's performance, we employ the train_test_split function from sklearn.model_selection to split the dataset into training and test sets. 
The model is then used to predict tumor diagnoses, with the results evaluated against the test set.

Saving the Model and Scaler

The trained model and scaler are saved using the joblib module. This step is crucial for deploying the model in the Streamlit app, ensuring consistency in predictions and data normalization.

Creating the Streamlit App

The Streamlit app is structured within a folder named 'app,' with the main file named 'app.py.' The app includes a container for organizing content and a sidebar with sliders for updating measurements. 
A radar chart is generated using the plotly library, displaying the measurements scaled appropriately. Additionally, the app provides predictions and probabilities based on user-inputted measurements.

Usage

Clone the repository.
Install dependencies using pip install -r requirements.txt.
Run the app using streamlit run app/app.py.
Input tumor measurements using the sliders.
View the radar chart and predictions for the tumor diagnosis.

Conclusion
This Streamlit app offers a user-friendly interface for predicting breast tumor diagnoses using a machine learning model trained on the Wisconsin Breast Cancer Dataset.
Feel free to explore, input your measurements, and gain insights into tumor predictions!
