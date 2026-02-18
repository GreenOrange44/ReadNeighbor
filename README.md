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

### Build and Push to Docker Hub

#### Step 1: Build the Docker Image

```bash
docker build -t readneighbor:1.0 .
```

#### Step 2: Tag the Image

```bash
docker tag readneighbor:1.0 tensor4/readneighbor:latest
docker tag readneighbor:1.0 tensor4/readneighbor:1.0
```

#### Step 3: Login to Docker Hub

```bash
docker login
```

Enter your Docker Hub credentials when prompted.

#### Step 4: Push to Docker Hub

```bash
docker push tensor4/readneighbor:latest
docker push tensor4/readneighbor:1.0
```

#### Step 5: Verify Your Image

Visit your Docker Hub repository: `https://hub.docker.com/r/tensor4/readneighbor`

---

## Docker Commands Reference

### View Local Images

```bash
docker images
```

### Run Container

```bash
docker run -p 8501:8501 tensor4/readneighbor:latest
```

### Run Container in Background

```bash
docker run -d -p 8501:8501 --name readneighbor tensor4/readneighbor:latest
```

### Check Running Containers

```bash
docker ps
```

### Stop a Container

```bash
docker stop container_id
```

### Remove a Container

```bash
docker rm container_id
```

### Pull Latest Image from Docker Hub

```bash
docker pull tensor4/readneighbor:latest
```

### Remove Local Image

```bash
docker rmi tensor4/readneighbor:latest
```

---

