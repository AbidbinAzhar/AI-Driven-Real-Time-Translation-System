# AI-Driven-Real-Time-Translation-System

## Real-Time Multilingual News Processing Pipeline Using Google News API and Transformer Models

NewsTranslate-AI is an end-to-end NLP pipeline that automates the collection, preprocessing, and translation of real-time business news articles. The system integrates external news APIs with transformer-based neural machine translation models to deliver automated English-to-Hindi translations of live business and financial news content.

Developed as part of a software engineering workflow, the project demonstrates API integration, data processing, natural language preprocessing, and deployment of state-of-the-art multilingual transformer models for automated language localization.

---

## Project Overview

Access to timely business and financial news is critical for informed decision-making. However, much of this information is published primarily in English, creating accessibility challenges for non-English-speaking audiences.

This project addresses that challenge by building a scalable pipeline that:

* Retrieves real-time business news articles
* Cleans and preprocesses textual data
* Performs neural machine translation
* Generates Hindi translations automatically
* Provides a reusable framework for multilingual news processing

The system showcases practical applications of Natural Language Processing (NLP), API integration, and transformer-based AI models in real-world software engineering environments.

---

## Engineering Highlights

* Designed a modular Python-based ETL pipeline for news processing
* Integrated third-party APIs for real-time data ingestion
* Automated JSON parsing and dataset generation
* Implemented text normalization and preprocessing workflows
* Built multilingual translation functionality using Hugging Face Transformers
* Leveraged Meta's mBART-50 model for neural machine translation
* Structured the application for maintainability and future language expansion
* Developed reusable components for scalable NLP workflows

---

## Key Features

* Real-time business news retrieval via Google News API
* Automated data cleaning and preprocessing
* News article filtering and retrieval by title
* English-to-Hindi translation using mBART-50
* Transformer-based neural machine translation
* Pandas-powered data processing pipeline
* Modular architecture for future enhancements
* Easily extensible to additional languages

---

## System Architecture

```text
User Request
      │
      ▼
Google News API
      │
      ▼
JSON Response Processing
      │
      ▼
Pandas Data Pipeline
      │
      ▼
Text Cleaning & Normalization
      │
      ▼
Article Selection
      │
      ▼
mBART Translation Engine
      │
      ▼
Hindi Translation Output
```

---

## Technology Stack

### Programming Language

* Python

### Data Processing

* Pandas
* JSON

### Natural Language Processing

* NLTK
* Regular Expressions (Regex)

### Machine Learning

* Hugging Face Transformers
* PyTorch
* mBART-50 Large Multilingual Model

### APIs

* RapidAPI
* Google News API

---

## Project Structure

```text
NewsTranslate-AI/
│
├── data/
│   └── News datasets
│
├── src/
│   ├── data_collection.py
│   ├── preprocessing.py
│   ├── translation.py
│   └── utils.py
│
├── notebooks/
│   └── Development experiments
│
├── requirements.txt
│
└── README.md
```

---

## Installation

Clone the repository:

```bash
git clone https://github.com/yourusername/NewsTranslate-AI.git

cd NewsTranslate-AI
```

Install dependencies:

```bash
pip install -r requirements.txt
```

Install Hugging Face Transformers:

```bash
pip install transformers sentencepiece torch
```

---

## API Configuration

Create a RapidAPI account and obtain your API key.

Replace:

```python
'x-rapidapi-key': "YOUR_API_KEY"
```

with your own API key before executing the pipeline.

For production deployments, environment variables are recommended:

```python
import os

API_KEY = os.getenv("RAPIDAPI_KEY")
```

---

## Usage

### Retrieve Latest Business News

```python
python data_collection.py
```

### Preprocess News Articles

```python
python preprocessing.py
```

### Generate Hindi Translations

```python
python translation.py
```

---

## Example Translation

### Input (English)

```text
Stocks rallied as investors reacted positively to new economic data.
```

### Output (Hindi)

```text
निवेशकों ने नए आर्थिक आंकड़ों पर सकारात्मक प्रतिक्रिया दी, जिससे शेयर बाजार में तेजी देखी गई।
```

---

## Data Preprocessing Pipeline

The preprocessing module performs:

### Punctuation Removal

Input:

```text
Stock Market Today: What's New?
```

Output:

```text
Stock Market Today Whats New
```

### Lowercase Normalization

Input:

```text
Stock Market Today
```

Output:

```text
stock market today
```

These preprocessing steps improve consistency and translation quality.

---

## Translation Model

This project utilizes Meta's multilingual transformer:

**facebook/mbart-large-50-one-to-many-mmt**

The model supports translation across 50 languages and provides high-quality contextual translations through sequence-to-sequence neural machine translation.

### Language Configuration

Source Language:

```text
en_XX
```

Target Language:

```text
hi_IN
```

---

## Outputs

The pipeline generates:

### Processed Data

* Cleaned news datasets
* Structured title and snippet tables
* Searchable news records

### Translation Outputs

* Hindi-translated news articles
* Translation dictionaries
* Model-generated multilingual outputs

---

## Business Applications

Potential use cases include:

* Financial news localization platforms
* Multilingual news aggregation services
* Media monitoring systems
* Cross-language content distribution
* International market intelligence platforms
* AI-powered news delivery applications
* Language accessibility solutions

---

## Technical Challenges and Solutions

### Challenge

News articles arrive in unstructured JSON formats with inconsistent text quality.

### Solution

Implemented automated preprocessing including punctuation removal, normalization, and structured dataset generation.

### Challenge

Supporting multilingual translation while preserving contextual meaning.

### Solution

Integrated Meta's mBART-50 multilingual transformer model for context-aware neural machine translation.

### Challenge

Building a reusable workflow for future language expansion.

### Solution

Designed a modular architecture separating ingestion, preprocessing, and translation components.

---

## Future Enhancements

* Multi-language translation support
* Sentiment analysis integration
* Topic classification
* Named Entity Recognition (NER)
* Translation quality evaluation metrics
* Streamlit-based web interface
* Docker deployment
* Real-time dashboard visualization
* GPU-optimized inference

---

## Reproducibility

The project supports reproducible execution through:

* Version-controlled source code
* Fixed dependency management
* Public API-based data retrieval
* Modular software architecture
* Deterministic processing workflows

---

## Intended Use

This project was developed as a software engineering and NLP application to demonstrate real-time data ingestion, language processing, and AI-powered translation workflows.

It is intended for educational, research, and prototype development purposes.

---

## Author

**Arif Bin Azhar**

Software Engineer | Bioinformatics Researcher | AI & Data Science Enthusiast

---

## Citation

If you use this project, please cite:

**Azhar AB.** NewsTranslate-AI: Real-Time Multilingual News Processing Pipeline Using Transformer Models. GitHub, 2026.
