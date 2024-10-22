# Water Quality Prediction App

This Flask-based web application collects environmental data such as temperature, pH, and pollutant levels, and sends it to an IBM Cloud Machine Learning model to predict water quality. The app features a form interface for users to input data, and it displays the predicted water quality score based on the submitted information.

## Table of Contents
- [Features](#features)
- [Technologies](#technologies)
- [Setup and Installation](#setup-and-installation)
- [Usage](#usage)
- [Form Parameters](#form-parameters)
- [IBM Cloud Integration](#ibm-cloud-integration)
- [Error Handling](#error-handling)
- [License](#license)

## Features

- Collects water quality data through a user-friendly form.
- Sends the data to an IBM Cloud Machine Learning API for predictions.
- Displays water quality predictions directly on the web page.
- Robust error handling and retry logic for API requests.
- Built-in CSRF protection and cross-origin support for secure usage.

## Technologies

- Python 3.x
- Flask
- Flask-WTF (Form validation and CSRF protection)
- Flask-CORS (Cross-Origin Resource Sharing)
- IBM Watson Machine Learning
- HTML5 (for the web interface)
- Requests (for HTTP requests to IBM Cloud)

## Setup and Installation

1. **Clone the Repository**:

   ```bash
   git clone https://github.com/yourusername/water-quality-prediction.git
   cd water-quality-prediction
