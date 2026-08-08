# Emotiva — Emotion Intelligence Dashboard

A premium, responsive dashboard for exploring multi-label emotion detection from text. Emotiva turns a message into an easy-to-understand emotion profile with confidence scores, visual analytics, and recent-analysis history.

![Status](https://img.shields.io/badge/status-demo-6D49F2?style=flat-square)
![Responsive](https://img.shields.io/badge/design-responsive-23C8CF?style=flat-square)
![NLP](https://img.shields.io/badge/domain-NLP-FF4E96?style=flat-square)

## Highlights

- **Multi-label emotion profile** — surfaces a primary emotion alongside related emotional signals.
- **Confidence visualization** — animated confidence bars and an interactive emotion spectrum chart.
- **Premium interface** — polished violet, cyan, and pink visual system with responsive layouts for mobile, tablet, and desktop.
- **Fast interaction flow** — analyze with a button or `Ctrl` + `Enter`; use built-in sample messages to explore the app.
- **Analysis history** — records recent messages, predicted emotions, confidence, and timestamps in the current session.
- **Model transparency panel** — clearly presents the intended BERT transformer architecture, model readiness, and inference specifications.

## Preview

Open `index.html` in any modern browser to use the dashboard. No installation or build step is required.

## Tech Stack

| Area | Technologies |
| --- | --- |
| Interface | HTML5, CSS3, JavaScript (ES6+) |
| Visual analytics | Chart.js |
| Design | Responsive CSS, custom glassmorphism UI, Google Fonts |
| Intended NLP backend | Python, BERT, Hugging Face Transformers, Scikit-learn, Pandas, NumPy |

## Run Locally

1. Clone the repository:

   ```bash
   git clone https://github.com/YOUR_USERNAME/emotiva-emotion-detection.git
   ```

2. Move into the project directory:

   ```bash
   cd emotiva-emotion-detection
   ```

3. Open `index.html` in your browser.

You can also use VS Code's **Live Server** extension for local development.

## Using the Dashboard

1. Enter or paste a message in the **Analyze text** field.
2. Select **Analyze emotion** or press `Ctrl` + `Enter`.
3. Review the primary emotion, multi-label confidence profile, emotional dimensions, and spectrum chart.
4. Check **Recent analyses** to compare previous results.

## Current Demo Behavior

The current version is a standalone front-end prototype. Its predictions are generated in the browser by lightweight keyword-based demo logic so it can be opened immediately without a server or model download.

For production-grade BERT inference, connect the UI to a Python API (for example, FastAPI or Flask) that loads a fine-tuned transformer model and returns multi-label probabilities. The existing dashboard is designed to display those probabilities directly.

## Suggested BERT Backend Architecture

```text
Browser dashboard
      │  POST /analyze { text }
      ▼
FastAPI / Flask service
      │
      ▼
Fine-tuned BERT multi-label classifier
      │
      ▼
Emotion probabilities + confidence metrics
      │
      ▼
Dashboard visualizations and history
```

## Future Enhancements

- Fine-tune `bert-base-uncased` on GoEmotions or a custom labeled dataset.
- Add an authenticated REST API for real BERT inference.
- Store user analysis history in SQLite or PostgreSQL.
- Add CSV/PDF export and shareable report links.
- Support batch analysis, language detection, and multilingual transformer models.

## Project Structure

```text
.
├── index.html       # Responsive dashboard, styles, and client-side interactions
└── README.md        # Project documentation
```

## License

This project is available for educational and portfolio use.
