# Health Insurance Premium Prediction

##  Project Overview  
This is an interactive machine learning application that predicts an individual's annual health insurance cost based on demographic, medical, and lifestyle inputs. The goal is to build an accurate machine-learning model that helps insurance companies estimate premiums efficiently.

## Features
- Predicts the Annual Premium Amount for a health insurance plan based on user inputs.

- Uses age-based model selection, with separate models and scalers for users aged ≤25 and >25 to improve accuracy.

- Built using machine learning regression models trained on a health insurance dataset.

- Applies custom preprocessing, including encoding of categorical features and scaling of numerical features.

- Provides an interactive Streamlit UI for users to input data and receive instant predictions.

- Loads pre-trained model artifacts for efficient and fast inference.

- Implements modular code structure with clear separation between data preprocessing, model loading, and prediction logic.


## Tech Stack
- Frontend: Streamlit
- Backend Logic: Python
- ML Models: Scikit-learn (with joblib for model loading)
- Deployment: Streamlit Cloud - https://mlproject-health-premium-prediction.streamlit.app/

##  Dataset Information  
The dataset contains the following features:  
- **age**: Age of the individual  
- **gender**: Male/Female  
- **region**: Geographic location of the individual -'Northwest' 'Southeast' 'Northeast' 'Southwest' 
- **marital_status**: Unmarried/Married  
- **number_of_dependants**: Count of dependents  
- **bmi_category**: Underweight/Normal/Overweight/Obesity 
- **smoking_status**: No Smoking/Regular/Occasional
- **employment_status**: Salaried/Freelancer/Self-Employed  
- **income_level**: <10L / 10L - 25L / >40L / 25L - 40L  
- **income_lakhs**: Income in lakhs (numerical value)  
- **medical_history**: Details of past medical conditions  
- **insurance_plan**: Type of insurance plan chosen - 'Bronze' /'Silver'/ 'Gold' 
- **annual_premium_amount**: Target variable (premium amount to be predicted)  

##  Project Setup  
### 1. Clone the Repository  
```bash
git clone https://github.com/neethu-codes/MLProject-Premium-Prediction.git
cd mlproject-premium-prediction
```
### 2. Create and Activate Virtual Environment
```bash
python -m venv venv  
source venv/bin/activate  # On Mac/Linux  
venv\Scripts\activate  # On Windows  
```
### 3. Install Dependencies
```bash
pip install -r requirements.txt 
```
### 4. Run the Streamlit App
```bash
streamlit run main.py
```
## Project Structure
```
mlproject-premium-prediction/
│── app/ 
│ ├── main.py # Streamlit application
│ ├── prediction_helper.py # Function to load and run the model
│── artifacts/
│ ├── model_rest.joblib # Pre-trained model for a subset of data
│ ├── model_young.joblib # Pre-trained model for a subset of data
│ ├── scaler_rest.joblib # Scaler used for subset of data
│ ├── scaler_young.joblib # Scaler used for subset of data
│── requirements.txt # Dependencies
│── README.md # Project documentation
│── notebooks/ # Jupyter notebooks for model training
│ ├── premium_prediction_rest_with_extra_info.ipynb # model training for age<=25
│ ├── premium_prediction_young_with_extra_info.ipynb # model training for age>25
```
## App Preview
Here’s a preview of the application:

<img src="health_app_screenshot.png" alt="App Screenshot" width="700">



