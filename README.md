# Lyrical — Song Lyrics Translation & Localization Platform

Lyrical is a context-aware lyrics localization platform for translating English song lyrics into **Hindi and Marathi** while preserving lyrical structure, meaning, and phonetic characteristics.

The platform combines **NLP-based translation, rhyme-aware lyric generation, and phonetic transliteration** through a web-based interface.

## Features

- **Lyrics Translation**  
  Translate English song lyrics into Hindi and Marathi using NLP models.

- **Rhyme-Aware Generation**  
  Generate localized verses while considering rhyme and lyrical structure.

- **Phonetic Transliteration**  
  Convert translated lyrics into phonetic representations for easier pronunciation.

- **Web-Based Interface**  
  Interactive React frontend for submitting lyrics and viewing generated results.

- **AI Model Services**  
  Python-based backend APIs for translation, generation, and transliteration workflows.

## Architecture

```text
                    ┌──────────────────────┐
                    │      React UI        │
                    │  Lyrics Input/Output │
                    └──────────┬───────────┘
                               │
                               │ REST API
                               ▼
                    ┌──────────────────────┐
                    │      FastAPI         │
                    │   Backend Services   │
                    └──────────┬───────────┘
                               │
                ┌──────────────┼──────────────┐
                ▼              ▼              ▼
          Translation     Rhyme-aware    Transliteration
             Model         Generation        Model
                │              │              │
                └──────────────┼──────────────┘
                               ▼
                         Generated Lyrics

```

## Technology Stack
### Frontend
- React
- JavaScript
- HTML/CSS
### Backend
- Python
- FastAPI
- REST APIs
### Machine Learning / NLP
- Hugging Face
- NLP translation models
- Rhyme-aware generation
- Phonetic transliteration
### Deployment
- Docker
- Containerized model services
### Dataset
A dataset of 200+ songs was curated and prepared for model development and evaluation.

The dataset contains lyrics across multiple genres and was used to support translation and lyric-generation experiments.

## Workflow
1. User submits English lyrics through the React interface.
2. Backend receives the request through FastAPI REST APIs.
3. Lyrics are processed and passed to the appropriate NLP model.
4. Translated lyrics are generated in Hindi or Marathi.
5. Rhyme-aware generation can be applied to produce localized verses.
6. Transliteration converts the generated lyrics into a phonetic representation when required.
7. Results are returned to the frontend for visualization.


## Project Structure
```
Lyrical/
├── frontend/              # React frontend
├── backend/               # FastAPI backend
├── models/                # NLP model services
├── data/                  # Dataset and preprocessing
├── docker/                # Containerization configuration
└── README.md

```

## Running the Project

1. Clone the repository
```
git clone <repository-url>
cd Lyrical
```

2. Start the backend
```
cd backend
pip install -r requirements.txt
uvicorn main:app --reload
```

3. Start the frontend
```
cd frontend
npm install
npm start
```

4. Using Docker

Model services can be containerized and started using:

```
docker compose up --build
```

## Example
### Input

```
English lyrics
        ↓
Translation
        ↓
Hindi / Marathi lyrics
        ↓
Rhyme-aware localization
        ↓
Phonetic transliteration
```


## Future Work
- Improve preservation of semantic and lyrical context during translation.
- Improve rhyme and meter consistency across generated verses.
- Expand support to additional Indian languages.
- Improve evaluation using human judgments for translation quality and lyrical fluency.
