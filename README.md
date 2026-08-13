# EmailGuardian

EmailGuardian is an intelligent email screening application that helps users identify suspicious messages before they are opened or acted upon. Instead of presenting itself as a simple spam classifier, the project focuses on **email safety**, **content inspection**, and **risk-aware message filtering** through a machine learning workflow and an interactive web interface.

## Why EmailGuardian?

Modern inboxes receive promotional emails, phishing attempts, scams, and malicious messages every day. EmailGuardian provides a lightweight desktop-friendly tool that analyzes email content and estimates whether a message is likely to be **Safe** or **Suspicious**, helping users make faster and safer decisions.

## What It Can Do

* Analyze raw email text instantly
* Classify messages as **Safe** or **Suspicious**
* Display a confidence score for every prediction
* Process multiple emails in a single upload
* Export analysis results for further review
* Run completely on your local machine

## Built With

* **Python**
* **Streamlit**
* **Scikit-learn**
* **Pandas**
* **NumPy**
* **BeautifulSoup4**

## Project Layout

```text
EmailGuardian/
│
├── app.py                  # Streamlit application
├── requirements.txt        # Dependencies
├── src/
│   ├── config/
│   ├── pipeline/
│   ├── components/
│   └── utils/
├── data/
├── outputs/
└── logs/
```

## Getting Started

### Clone

```bash
git clone https://github.com/YOUR_USERNAME/EmailGuardian.git
cd EmailGuardian
```

### Create a virtual environment

```bash
python -m venv .venv
```

Activate it:

**Windows PowerShell**

```powershell
.\\.venv\\Scripts\\Activate.ps1
```

### Install packages

```bash
pip install -r requirements.txt
```

## Launch the App

```bash
streamlit run app.py
```

Once started, open the local address displayed in the terminal (typically `http://localhost:8501`).

## How EmailGuardian Works

1. Email content is collected from user input or uploaded files.
2. The text is cleaned and normalized.
3. A TF-IDF feature extractor converts the content into numerical vectors.
4. A trained machine learning model evaluates the message.
5. The interface presents a **Safe/Suspicious** verdict along with a confidence estimate.

## Retraining the Model

To train EmailGuardian on a different dataset:

```bash
python -m src.pipeline.training_pipeline
```

New model artifacts are stored inside the `outputs/` directory.

## Roadmap

* Phishing URL inspection
* Attachment risk detection
* Email source reputation analysis
* Transformer-based language models
* FastAPI deployment
* User dashboard with scan history

## License

Released under the **MIT License**.

## Author

**Yashvi Gheewala**

GitHub: https://github.com/YashviG99
