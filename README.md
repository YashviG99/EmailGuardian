# SmartSpamShield – AI Spam Email Detection System

SmartSpamShield is a machine learning web application that detects whether an email is **Spam** or **Ham (Legitimate)** using natural language processing and a trained classification model. The application provides a clean Streamlit interface for real-time predictions and supports batch analysis of email files.

## Features

* Real-time spam email prediction
* Confidence score for each prediction
* Batch processing of multiple emails
* TF-IDF text vectorization
* Trained machine learning classifier (SVM / Logistic Regression)
* Interactive Streamlit dashboard
* Simple and modular project structure

## Tech Stack

* **Python 3.11**
* **Streamlit**
* **Scikit-learn**
* **Pandas**
* **NumPy**
* **BeautifulSoup4**

## Project Structure

```text
SmartSpamShield/
├── app.py
├── requirements.txt
├── src/
│   ├── components/
│   ├── pipeline/
│   ├── config/
│   └── utils/
├── data/
├── outputs/
└── logs/
```

## Installation

1. Clone the repository

```bash
git clone https://github.com/YOUR_USERNAME/SmartSpamShield.git
cd SmartSpamShield
```

2. Create and activate a virtual environment

```bash
python -m venv .venv
```

Windows PowerShell:

```powershell
.\\.venv\\Scripts\\Activate.ps1
```

3. Install dependencies

```bash
pip install -r requirements.txt
```

## Run the Application

Start the Streamlit application:

```bash
streamlit run app.py
```

Open the local URL shown in the terminal (usually `http://localhost:8501`).

## How It Works

1. The user enters email text or uploads an email file.
2. The text is cleaned and preprocessed.
3. A TF-IDF vectorizer converts the text into numerical features.
4. The trained machine learning model predicts whether the email is **Spam** or **Ham**.
5. The prediction and confidence score are displayed in the interface.

## Model Training

To retrain the model with a new dataset:

1. Place the dataset inside the `data/` directory.
2. Run the training pipeline:

```bash
python -m src.pipeline.training_pipeline
```

The trained model and vectorizer will be saved inside the `outputs/` directory.

## Future Improvements

* Email attachment analysis
* Phishing URL detection
* Email sender reputation scoring
* Deep learning (LSTM/BERT) models
* REST API deployment with FastAPI
* User authentication and prediction history

## License

This project is licensed under the **MIT License**.

## Author

**Yashvi Gheewala**

GitHub: https://github.com/YashviG99
