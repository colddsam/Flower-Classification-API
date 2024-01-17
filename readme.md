# Flower Classification API

---

## Overview

This project is a RESTful API built with FastAPI and TensorFlow Lite for classifying flower images into five categories: daisy, dandelion, rose, sunflower, and tulip. The API takes an image URL as input and returns the predicted flower category and a confidence score.

---

## API Endpoints

### POST /

This endpoint is the root page of the API. It returns a simple message indicating that the API is operational.

### GET /predict/?URL={image_url}

This endpoint is used to make predictions. It takes an image URL as a query parameter and returns the predicted flower category and confidence score.

The URL must be a valid URL pointing to an image file. Supported image formats include JPG, PNG, and GIF.

---

## Usage

To use the API, send a GET request to the `/predict/` endpoint with the image URL as a query parameter. The API will return a JSON response with the predicted flower category and confidence score.

For example, the following curl command sends a GET request to the API with the image URL `https://upload.wikimedia.org/wikipedia/commons/thumb/4/41/Rosa_chinensis_var._semperflorens_03.jpg/1200px-Rosa_chinensis_var._semperflorens_03.jpg`:

```
curl -X GET "http://localhost:8000/predict/?URL=https://upload.wikimedia.org/wikipedia/commons/thumb/4/41/Rosa_chinensis_var._semperflorens_03.jpg/1200px-Rosa_chinensis_var._semperflorens_03.jpg"
```

The API will respond with a JSON response similar to the following:

```
{
  "prediction": "rose",
  "confidence": 0.99
}
```

---

## Prerequisites

To run this project, you will need the following:

* Python 3.8 or later
* TensorFlow 2.4 or later
* FastAPI
* uvicorn

---

## Installation

To install the required dependencies, run the following command in your terminal:

```
pip install -r requirements.txt
```

---

## Running the API

To run the API, follow these steps:

1. Clone this repository to your local machine.
2. Open a terminal window and navigate to the project directory.
3. Start the API by running the following command:

```
uvicorn main:app --reload
```

The API will start running on `http://localhost:8000`.

---

## Contributing

Contributions are welcome! Please read the [contributing guidelines](https://github.com/your-username/flower-classification-api/blob/main/CONTRIBUTING.md) before submitting a pull request.

---

## License

This project is licensed under the MIT License. See the [LICENSE](https://github.com/your-username/flower-classification-api/blob/main/LICENSE) file for details.