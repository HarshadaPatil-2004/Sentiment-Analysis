# Emotiva — Emotion Intelligence Dashboard

**Emotiva** is a premium, responsive emotion intelligence dashboard designed to analyze text and present an easy-to-understand emotional profile with confidence scores, visual analytics, and recent-analysis history.

The current version is a standalone front-end prototype that demonstrates the complete user experience for multi-label emotion analysis.

## ✨ Highlights

* **Multi-label emotion profile** — Displays a primary emotion along with related emotional signals.
* **Confidence visualization** — Presents animated confidence bars and an interactive emotion spectrum chart.
* **Premium responsive interface** — Modern violet, cyan, and pink visual design with layouts optimized for desktop, tablet, and mobile.
* **Fast interaction flow** — Analyze text using the button or `Ctrl + Enter`.
* **Sample messages** — Built-in examples make it easy to explore the dashboard.
* **Analysis history** — Stores recent analyses during the current browser session.
* **Model transparency** — Includes a panel describing the intended BERT-based architecture and inference workflow.

## 🚀 Live Demo

Open `index.html` in a modern web browser.

No installation, backend server, or model download is required for the current demo.

## 🛠️ Tech Stack

| Area                 | Technologies                                |
| -------------------- | ------------------------------------------- |
| Frontend             | HTML5, CSS3, JavaScript (ES6+)              |
| Visualization        | Chart.js                                    |
| UI / Design          | Responsive CSS, Glassmorphism, Google Fonts |
| Intended NLP Backend | Python, BERT, Hugging Face Transformers     |
| Data / ML            | Scikit-learn, Pandas, NumPy                 |

## 📂 Project Structure

```text
Sentiment-Analysis/
│
├── index.html
│
└── outputs/
    └── emotioniq/
        ├── index.html
        ├── app.js
        └── styles.css
```

## 💻 Run Locally

### 1. Clone the repository

```bash
git clone https://github.com/HarshadaPatil-2004/Sentiment-Analysis.git
```

### 2. Open the project

```bash
cd Sentiment-Analysis
```

### 3. Launch the dashboard

Open:

```text
index.html
```

in any modern web browser.

Alternatively, use the **Live Server** extension in VS Code for local development.

## 🎯 Using the Dashboard

1. Enter or paste a message into the **Analyze Text** field.
2. Click **Analyze Emotion** or press `Ctrl + Enter`.
3. Review the predicted primary emotion and related emotional signals.
4. Explore the confidence scores and emotion spectrum visualization.
5. Check **Recent Analyses** to review previous results from the current session.

## 🔍 Current Demo Behavior

The current implementation is a **standalone front-end prototype**.

The emotion predictions are generated in the browser using lightweight keyword-based demonstration logic. This allows the dashboard to run immediately without requiring a backend server, model download, or GPU.

The interface is designed so that the demo logic can later be replaced with real machine-learning inference.

## 🤖 Planned BERT Backend

For production-grade emotion classification, the dashboard can be connected to a Python API such as **FastAPI** or **Flask**.

The planned architecture is:

```text
Browser Dashboard
       │
       │ POST /analyze
       │ { "text": "..." }
       ▼
FastAPI / Flask API
       │
       ▼
Fine-tuned BERT
Multi-label Classifier
       │
       ▼
Emotion Probabilities
       │
       ▼
Dashboard Visualizations
       │
       ▼
Analysis History
```

The backend can return multi-label emotion probabilities that are directly consumed by the existing dashboard visualizations.

## 🔮 Future Enhancements

* Fine-tune `bert-base-uncased` on the GoEmotions dataset or a custom emotion dataset.
* Integrate a real BERT-based multi-label classification API.
* Add REST API authentication.
* Store analysis history using SQLite or PostgreSQL.
* Add CSV and PDF report export.
* Support batch text analysis.
* Add language detection.
* Support multilingual transformer models.
* Deploy the complete application using a cloud platform.

## 📸 Dashboard Features

The dashboard is designed to provide:

* Primary emotion detection
* Related emotion signals
* Confidence scores
* Emotion spectrum visualization
* Recent analysis history
* Responsive interface
* Sample text analysis
* Keyboard shortcut support

## 📌 Project Status

**Current Status:** Front-end prototype

The user interface and visualization layer are implemented. The current browser-based emotion detection uses demonstration logic, while integration with a fine-tuned BERT model is planned as a future enhancement.

