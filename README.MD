# ML End-to-End Project: Modular Programming Approach

## Project Overview
This repository contains an end-to-end machine learning project implemented using a modular programming approach. The project is structured following industry best practices, making it maintainable, scalable, and reproducible.

## Project Structure
```
ML-End-to-End-Project_Modular_Programming/
│
├── .github/                    # GitHub Actions workflows for CI/CD
│
├── artifacts/                  # Generated model artifacts and data
│   ├── data_transformation/
│   ├── model_trainer/
│   └── ...
│
├── config/                     # Configuration files
│   └── config.yaml             # Main configuration parameters
│
├── logs/                       # Application logs
│
├── notebook/                   # Jupyter notebooks for exploration
│   ├── data/                   # Data used in notebooks
│   └── EDA.ipynb               # Exploratory Data Analysis
│
├── src/                        # Source code for the project
│   ├── ML_Project/             # Main package
│   │   ├── components/         # Modular components of the ML pipeline
│   │   │   ├── data_ingestion.py
│   │   │   ├── data_transformation.py
│   │   │   ├── data_validation.py
│   │   │   └── model_trainer.py
│   │   │
│   │   ├── config/             # Configuration handling
│   │   │   └── configuration.py
│   │   │
│   │   ├── constants/          # Project constants
│   │   │   └── __init__.py
│   │   │
│   │   ├── entity/             # Data models and entity definitions
│   │   │   ├── artifacts_entity.py
│   │   │   └── config_entity.py
│   │   │
│   │   ├── exception/          # Custom exception handling
│   │   │   └── __init__.py
│   │   │
│   │   ├── logger/             # Logging functionality
│   │   │   └── __init__.py
│   │   │
│   │   ├── pipeline/           # ML pipelines
│   │   │   ├── prediction_pipeline.py
│   │   │   ├── stage_01_data_ingestion.py
│   │   │   ├── stage_02_data_validation.py
│   │   │   ├── stage_03_data_transformation.py
│   │   │   └── stage_04_model_trainer.py
│   │   │
│   │   ├── utils/              # Utility functions
│   │   │   └── __init__.py
│   │   │
│   │   └── __init__.py
│   │
│   └── __init__.py
│
├── templates/                  # Web application templates
│   └── index.html
│
├── .gitignore                  # Git ignore file
├── app.py                      # Flask application entry point
├── main.py                     # Main entry point for the ML pipeline
├── params.yaml                 # Hyperparameters for the models
├── README.md                   # Project documentation
├── requirements.txt            # Project dependencies
└── setup.py                    # Package setup configuration
```

## Modular Components Explanation

### 1. Components
The `src/ML_Project/components/` directory contains the core building blocks of the ML pipeline:

- **data_ingestion.py**: Handles data collection and loading from various sources.
- **data_validation.py**: Validates data schema, checks for drift, and ensures data quality.
- **data_transformation.py**: Performs feature engineering, preprocessing, and transformations.
- **model_trainer.py**: Implements model training, tuning, and evaluation.

### 2. Pipeline
The `src/ML_Project/pipeline/` directory orchestrates the entire ML workflow:

- **stage_01_data_ingestion.py**: Executes the data ingestion process.
- **stage_02_data_validation.py**: Manages data validation procedures.
- **stage_03_data_transformation.py**: Coordinates data transformation activities.
- **stage_04_model_trainer.py**: Oversees model training and evaluation.
- **prediction_pipeline.py**: Handles making predictions with the trained model.

### 3. Entity
The `src/ML_Project/entity/` directory defines data structures:

- **config_entity.py**: Contains dataclasses for configuration settings.
- **artifacts_entity.py**: Defines structures for pipeline outputs and artifacts.

### 4. Configuration
The project uses a configuration-driven approach:

- **config/config.yaml**: Central configuration file.
- **src/ML_Project/config/configuration.py**: Loads and manages configuration settings.
- **params.yaml**: Stores model hyperparameters.

### 5. Utils, Logger, and Exception
- **utils**: Contains helper functions used across the project.
- **logger**: Provides consistent logging functionality.
- **exception**: Implements custom exception handling for better error reporting.

## Getting Started

### Prerequisites
- Python 3.7+
- pip or conda for package management

### Installation
1. Clone the repository:
```bash
git clone https://github.com/tejask0512/ML-End-to-End-Project_Modular_Programming.git
cd ML-End-to-End-Project_Modular_Programming
```

2. Install dependencies:
```bash
pip install -r requirements.txt
```

3. Install the package in development mode:
```bash
pip install -e .
```

### Running the Pipeline
Execute the full ML pipeline:
```bash
python main.py
```

### Running the Web Application
Start the Flask application:
```bash
python app.py
```

## Project Workflow

1. **Data Ingestion**: Raw data is collected, processed, and stored.
2. **Data Validation**: Ensures data quality and schema compliance.
3. **Data Transformation**: Features are processed and transformed for model training.
4. **Model Training**: ML models are trained, evaluated, and the best model is selected.
5. **Prediction**: The trained model is used for making predictions on new data.

## Benefits of Modular Programming Approach

1. **Maintainability**: Each component has a specific responsibility, making code easier to maintain.
2. **Reusability**: Components can be reused across different projects.
3. **Testability**: Isolated components are easier to test.
4. **Scalability**: Easy to add new components or modify existing ones.
5. **Collaboration**: Multiple developers can work on different components simultaneously.

## Contributing
1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## License
This project is licensed under the MIT License - see the LICENSE file for details.

## Acknowledgments
- [Scikit-learn](https://scikit-learn.org/)
- [Pandas](https://pandas.pydata.org/)
- [Flask](https://flask.palletsprojects.com/)
