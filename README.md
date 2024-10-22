Water Quality Prediction App
This Flask-based web application collects environmental data such as temperature, pH, and pollutant levels, and sends it to an IBM Cloud Machine Learning model to predict water quality. The app features a form interface for users to input data, and it displays the predicted water quality score based on the submitted information.

Table of Contents
Features
Technologies
Setup and Installation
Usage
Form Parameters
IBM Cloud Integration
Error Handling
License
Features
Collects water quality data through a user-friendly form.
Sends the data to an IBM Cloud Machine Learning API for predictions.
Displays water quality predictions directly on the web page.
Robust error handling and retry logic for API requests.
Built-in CSRF protection and cross-origin support for secure usage.
Technologies
Python 3.x
Flask
Flask-WTF (Form validation and CSRF protection)
Flask-CORS (Cross-Origin Resource Sharing)
IBM Watson Machine Learning
HTML5 (for the web interface)
Requests (for HTTP requests to IBM Cloud)
Setup and Installation
Clone the Repository:

bash
Copy code
git clone https://github.com/yourusername/water-quality-prediction.git
cd water-quality-prediction
Create a Virtual Environment:

bash
Copy code
python3 -m venv venv
source venv/bin/activate  # For Windows, use `venv\Scripts\activate`
Install Dependencies:

bash
Copy code
pip install -r requirements.txt
IBM Cloud Setup:

Ensure you have an IBM Cloud account.
Set up an IBM Watson Machine Learning service.
Replace the API_KEY and the URL in the app.py file with your IBM Cloud API credentials and deployment URL.
Environment Configuration:

Update the secret key and the IBM API credentials in your app.py file:

python
Copy code
app.secret_key = 'your_secret_key'
API_KEY = "your_ibm_cloud_api_key"
Run the Application:

bash
Copy code
flask run
By default, the app will run on http://127.0.0.1:5000/.

Usage
Once the application is running, access it via your browser.
Fill out the form with the required environmental parameters (e.g., temperature, pH, conductivity, etc.).
Click the Predict button to submit the data to the model.
The app will return the predicted water quality score.
Form Parameters
The form expects the following parameters:

State: The state or region of water collection.
Temp: Water temperature (°C).
D.O.: Dissolved Oxygen level (mg/L).
PH: pH level of the water.
CONDUCTIVITY: Electrical conductivity of the water (μS/cm).
B.O.D.: Biological Oxygen Demand (mg/L).
NITRATE_NITRITE: Nitrate/Nitrite levels (mg/L).
FECAL_COLIFORM: Fecal Coliform levels (CFU/100mL).
TOTAL_COLIFORM: Total Coliform levels (CFU/100mL).
IBM Cloud Integration
This application integrates with IBM Watson Machine Learning to make predictions based on input data. The model prediction is fetched using an IBM Cloud IAM token, which is generated using the provided API_KEY.

IBM Cloud IAM URL: https://iam.cloud.ibm.com/identity/token
IBM Cloud Model Prediction API URL: Update with your IBM model's deployment URL.
Error Handling
The app has built-in error handling mechanisms for various potential issues, including:

Invalid form input or missing data.
Issues with IBM Cloud API responses.
Retry logic to handle transient network issues.
In case of an error, the user will see an appropriate error message on the web page.

License
This project is licensed under the MIT License - see the LICENSE file for details.
