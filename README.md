# Spam Detection API

## Overview

This API utilizes a machine learning model to predict whether an email is spam or not based on its content. Built using Python and Flask, it's designed for educational purposes and simple demonstrations.

## Datasets

The datasets used in this project are too large to be hosted on GitHub. You can access them via the following Dropbox link:

[[Insert shareable link here](https://www.dropbox.com/scl/fo/ftkdawlhffyjv15if9d3p/AGvvf5ZDzsN8uC86GD9OsOE?rlkey=8irdn7czo1nzgifcsitbyboll&st=dt49fqs5&dl=0)]

Please note that you may need to create a Dropbox account to access the files.

## Features

* **Spam Prediction**: Determines if an email text is spam.
* **Feedback Submission**: Allows users to submit feedback on the prediction accuracy.

## Getting Started

### Prerequisites

* Python 3.6+
* Flask
* pandas
* scikit-learn
* joblib
* TextBlob

### Installation

1. Clone the repository: `git clone (link unavailable) and cd spam-detection-api`
2. Set up a Python virtual environment (optional but recommended): `python -m venv venv` and `source venv/bin/activate` (On Windows use `venv\Scripts\activate`)
3. Install dependencies: `pip install -r requirements.txt`
4. Run the application: `python app.py`

## Usage

The API has two main endpoints:

### Predict

* **Endpoint**: `/predict`
* **Method**: `POST`
* **Description**: Receives an email text and predicts whether it is spam or not.
* **Payload**: `{ "email": "example@example.com" }`
* **Response**: `{ "result": "spam"  // or "ham" }`

### Feedback

* **Endpoint**: `/feedback`
* **Method**: `POST`
* **Description**: Allows users to provide feedback on the predictions.
* **Payload**: `{ "email": "example@example.com", "is_spam": true  // or false }`
* **Response**: `{ "success": true }`

## Testing

To test the endpoints, you can use tools like Postman or cURL: `curl -X POST -H "Content-Type: application/json" -d '{"email":"example@example.com"}' http://localhost:5000/predict`

## Contributing

Contributions to the Spam Detection API are welcome! Please fork the repository and submit pull requests with any enhancements or bug fixes.

## Contact

For any queries, please email us at [sl10158@nyu.edu](mailto:sl10158@nyu.edu)
