# Deploy-ML-projects-using-FastAPI

Here is a possible readme.md file for the Github repository shown on the current webpage:

# Deploy-ML-projects-using-FastAPI

This repository contains the code and instructions for deploying a machine learning model using FastAPI, a modern, fast, and high-performance web framework for building APIs.

## Project overview

The project uses a pre-trained model to predict the survival of passengers on the Titanic based on their features such as age, sex, class, fare, etc. The model is packaged as a Python wheel file using `setuptools` and `wheel`. The model is then served as a RESTful API using FastAPI, which allows users to send requests and receive predictions in JSON format. The API also provides interactive documentation using Swagger UI and ReDoc.

## Requirements

- Python 3.6 or higher
- FastAPI
- Uvicorn
- Requests
- Pandas
- Numpy

You can install the required packages using `pip install -r requirements.txt`.

## Usage

To run the API server, execute the following command:

`uvicorn app.main:app --reload`

This will start the server at `http://127.0.0.1:8000`.

To test the API, you can use the interactive documentation at `http://127.0.0.1:8000/docs` or `http://127.0.0.1:8000/redoc`, or use a tool like `curl` or `Postman`.

For example, you can send a POST request to `http://127.0.0.1:8000/predict` with the following JSON body:

```json
{
  "PassengerId": 1,
  "Pclass": 3,
  "Name": "Braund, Mr. Owen Harris",
  "Sex": "male",
  "Age": 22,
  "SibSp": 1,
  "Parch": 0,
  "Ticket": "A/5 21171",
  "Fare": 7.25,
  "Cabin": null,
  "Embarked": "S"
}
```

And you will receive a JSON response like this:

```json
{
  "PassengerId": 1,
  "prediction": 0,
  "probability": 0.087
}
```

Where `prediction` is either 0 (did not survive) or 1 (survived), and `probability` is the corresponding probability.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
## Contributing

If you have a Data Science mini-project that you'd like to share, please follow the guidelines in [CONTRIBUTING.md](https://github.com/Praveen76/Data-Science-Mini-Projects/blob/main/contributing.md).

## Code of Conduct
Please adhere to our [Code of Conduct](https://github.com/Praveen76/Data-Science-Mini-Projects/blob/main/CODE_OF_CONDUCT.md) in all your interactions with the project.

## Contact

For questions or inquiries, feel free to contact me on [Linkedin](https://www.linkedin.com/in/praveen-kumar-anwla-49169266/).

## **About Me**:
I’m a seasoned Data Scientist and founder of [TowardsMachineLearning.Org](https://towardsmachinelearning.org/). I've worked on various Machine Learning, NLP, and cutting-edge deep learning frameworks to solve numerous business problems.

