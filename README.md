# ReadNeighbor - End-to-End Book Recommendation System

A machine learning-powered book recommendation system built with Streamlit and Scikit-learn. This project implements a complete ML pipeline with data ingestion, validation, transformation, and model training to provide personalized book recommendations.

## Project Architecture

```
ReadNeighbor/
├── components/           # ML pipeline stages
│   ├── stage_00_data_ingestion.py
│   ├── stage_01_data_validation.py
│   ├── stage_02_data_transformation.py
│   └── stage_03_model_trainer.py
├── config/              # Configuration management
│   └── configuration.py
├── entity/              # Data entity definitions
├── logger/              # Logging utilities
├── exception/           # Custom exception handlers
├── pipeline/            # Training pipeline orchestration
├── utils/               # Utility functions
├── app.py               # Streamlit web application
├── main.py              # Entry point for ML pipeline
└── config.yaml          # Configuration parameters
```

## Local Setup

### Prerequisites
- Python 3.12+
- conda or pip virtual environment
- Git

### STEP 1: Clone the Repository

```bash
git clone https://github.com/GreenOrange44/ReadNeighbor
cd ReadNeighbor
```

### STEP 2: Create a Conda Environment

```bash
conda create -n readneighbor python=3.12 -y
conda activate readneighbor
```

### STEP 3: Install Dependencies

```bash
pip install -r requirements.txt
```

### STEP 4: Run the Application

```bash
streamlit run app.py
```

The app will be available at `http://localhost:8501`

---

## Docker Deployment

### Quick Start with Docker Hub

Pull and run the pre-built image directly from Docker Hub:

```bash
docker run -p 8501:8501 tensor4/readneighbor:latest
```

Then visit `http://localhost:8501` in your browser.
