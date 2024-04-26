Email Spam Detection API

Overview

This document provides comprehensive user documentation for the Spam Detection API. This API utilizes a machine learning model to predict whether an email is spam or not based on its content. The application is built using Python and Flask, and it is designed for educational purposes and simple demonstrations.

Features

Spam Prediction: Determines if an email text is spam.
Feedback Submission: Allows users to submit feedback on the prediction accuracy.
Getting Started

Prerequisites

To run this application locally, you will need:

Python 3.6+
Flask
pandas
scikit-learn
joblib
TextBlob

Installation

1. Clone the repository:

git clone https://yourrepository.com/spam-detection-api.git
cd spam-detection-api

2. Set up a Python virtual environment (optional but recommended):

python -m venv venv
source venv/bin/activate  # On Windows use `venv\Scripts\activate`

3. Install dependencies:

pip install -r requirements.txt

4. Run the application:

python app.py

Usage

The API has two main endpoints:

1. Predict
Endpoint: /predict
Method: POST
Description: Receives an email text and predicts whether it is spam or not.

Payload:

{
  "email": "example@example.com"
}

Response:

{
  "result": "spam"  // or "ham"
}

2. Feedback

Endpoint: /feedback
Method: POST
Description: Allows users to provide feedback on the predictions.
Payload:

{
  "email": "example@example.com",
  "is_spam": true  // or false
}

Response:

{
  "success": true
}

Testing

To test the endpoints, you can use tools like Postman or cURL:

curl -X POST -H "Content-Type: application/json" -d '{"email":"example@example.com"}' http://127.0.0.1:5000/predict

Contributing

Contributions to the Spam Detection API are welcome! Please fork the repository and submit pull requests with any enhancements or bug fixes.

Contact

For any queries, please email us at sl10158@nyu.edu


