# ScoreSage - Student Performance Predictor

This project predicts student academic performance in mathematics based on various demographic and socioeconomic factors such as gender, ethnicity, parental level of education, lunch type, and test preparation course.

## Overview

Understanding the factors that influence academic outcomes helps educators and institutions design targeted interventions. This project implements an end-to-end machine learning pipeline that includes data ingestion, preprocessing, model training with hyperparameter tuning, and a Flask web application for interactive inference.

## Features

- End-to-end machine learning pipeline with automated data preprocessing and model evaluation.
- Analysis of demographic and educational background impact on math test scores.
- Interactive Flask web interface to test predictions in real-time.
- Modular architecture with distinct ingestion, transformation, training, and prediction modules.

## Project Structure

```text
├── artifacts/              # Serialized models, preprocessors, and datasets
├── catboost_info/          # Training logs and metrics
├── Notebook/               # Exploratory Data Analysis & experiments
│   ├── 1 . EDA STUDENT PERFORMANCE .ipynb
│   ├── 2. MODEL TRAINING.ipynb
│   └── data/
│       └── stud.csv
├── src/                    # Application source code
│   ├── components/         # Ingestion, transformation, and training logic
│   ├── pipeline/           # Inference and training pipelines
│   ├── exception.py        # Custom exception handler
│   ├── logger.py           # Logging configuration
│   └── utils.py            # Utility helper functions
├── static/                 # Static CSS stylesheets
├── templates/              # HTML frontend templates
├── app.py                  # Flask entry point
├── requirements.txt        # Project dependencies
└── setup.py                # Package setup configuration
```

## Setup and Installation

1. Create and activate a Python virtual environment:
   ```bash
   python -m venv venv
   # On Windows:
   venv\Scripts\activate
   # On macOS/Linux:
   source venv/bin/activate
   ```

2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

## Running the Application

1. Start the Flask server:
   ```bash
   python app.py
   ```

2. Open your web browser and navigate to:
   ```text
   http://localhost:5000
   ```

3. Fill out the student details form to receive the predicted mathematics score.

## Dataset & Model Training

- **Dataset**: Student exam performance data containing demographic factors and test scores across subjects.
- **Models Evaluated**: Linear Regression, Decision Tree, Random Forest, CatBoost, AdaBoost, XGBoost, and Gradient Boosting.
- **Selected Model**: Tuned regressor achieving ~85% R² score on the test set.
