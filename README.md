# AI-Driven-Real-Time-Translation-System

# NewsTranslate-AI

## Multilingual Business News Translation Pipeline Using Google News API and mBART

NewsTranslate-AI is a Natural Language Processing (NLP) pipeline that automatically retrieves real-time business news articles, preprocesses textual content, and generates Hindi translations using Meta's multilingual mBART transformer model.

The project demonstrates an end-to-end workflow for multilingual information processing by integrating live news acquisition, text normalization, and neural machine translation. It serves as a practical example of applying transformer-based NLP models to improve accessibility of business and financial information across language barriers.

---

# Scientific Motivation

Business and financial news play a critical role in decision-making for investors, organizations, and the general public. However, a substantial portion of online news content is published primarily in English, limiting accessibility for non-English-speaking audiences.

Recent advances in multilingual transformer architectures have enabled effective machine translation across multiple languages. This project explores the integration of real-time news retrieval and transformer-based translation to automatically generate Hindi translations of English business news content.

The pipeline provides a reproducible framework for:

* Automated collection of real-time business news
* Text preprocessing and normalization
* Transformer-based machine translation
* Cross-lingual information access
* Educational and research-oriented NLP experimentation

---

# Project Objectives

The primary objectives of this project are:

* Retrieve business news articles from online sources in real time
* Process and clean raw textual content
* Translate English news content into Hindi
* Demonstrate the application of multilingual transformer models
* Build a modular NLP workflow that can be extended to additional languages and domains

---

# Key Features

* Real-time business news retrieval through Google News API (RapidAPI)
* Automated JSON parsing and structured dataset creation
* Text preprocessing and normalization pipeline
* News article search and selection functionality
* English-to-Hindi translation using mBART-50
* Transformer-based neural machine translation workflow
* Modular Python implementation
* Reproducible NLP pipeline

---

# Workflow

```text
Google News API
        │
        ▼
 News Retrieval
        │
        ▼
 JSON Processing
        │
        ▼
 Dataset Creation
        │
        ▼
 Text Cleaning
        │
        ▼
 Article Selection
        │
        ▼
 mBART Tokenization
        │
        ▼
 English → Hindi Translation
        │
        ▼
 Translated Output
```

---

# Dataset Characteristics

Source:

* Google News API (RapidAPI)

Domain:

* Business and Financial News

Input Language:

* English

Target Language:

* Hindi

Data Format:

* JSON News Articles

The dataset is collected dynamically through API requests and therefore varies depending on retrieval time and news availability.

---

# Model Selection

This project utilizes:

**facebook/mbart-large-50-one-to-many-mmt**

mBART was selected because it is a multilingual sequence-to-sequence transformer model trained on multiple languages, including English and Hindi. The model enables direct multilingual translation without requiring separate language-specific architectures.

Source Language Code:

```text
en_XX
```

Target Language Code:

```text
hi_IN
```

---

# Technologies Used

## Programming & Data Processing

* Python
* Pandas
* JSON

## Natural Language Processing

* NLTK
* Regular Expressions (Regex)

## Deep Learning

* Hugging Face Transformers
* PyTorch
* mBART-50

## Data Source

* Google News API (RapidAPI)

---

# Project Structure

```text
NewsTranslate-AI/
│
├── data/
│   └── Retrieved news datasets
│
├── notebooks/
│   └── Translation experiments
│
├── src/
│   ├── data_collection.py
│   ├── preprocessing.py
│   ├── translation.py
│   └── utils.py
│
├── requirements.txt
│
└── README.md
```

---

# Installation

Clone the repository:

```bash
git clone https://github.com/yourusername/NewsTranslate-AI.git

cd NewsTranslate-AI
```

Install dependencies:

```bash
pip install -r requirements.txt
```

Install transformer libraries:

```bash
pip install transformers sentencepiece torch
```

---

# API Configuration

Create a RapidAPI account and obtain an API key.

Replace:

```python
'x-rapidapi-key': "YOUR_API_KEY"
```

with your personal API key before running the pipeline.

---

# Usage

### Retrieve News Articles

```bash
python data_collection.py
```

### Preprocess Text

```bash
python preprocessing.py
```

### Translate News Articles

```bash
python translation.py
```

---

# Example Translation

### Input (English)

```text
stocks rallied as investors reacted positively to economic data
```

### Output (Hindi)

```text
आज शेयर बाजार में निवेशकों ने आर्थिक आंकड़ों पर सकारात्मक प्रतिक्रिया दी जिससे बाजार में तेजी देखी गई।
```

---

# Text Preprocessing

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

### Lowercase Conversion

Input:

```text
Stock Market Today
```

Output:

```text
stock market today
```

These preprocessing steps improve consistency prior to translation.

---

# Outputs

The pipeline generates:

* Retrieved business news articles
* Cleaned and normalized text datasets
* English news content
* Hindi translated news content
* Structured translation outputs

---

# Applications

Potential applications include:

* Multilingual news aggregation platforms
* Business and financial news translation systems
* Cross-lingual information access
* Educational NLP demonstrations
* Research-oriented multilingual processing workflows

---

# Relevance to Multilingual NLP

This project demonstrates the practical application of multilingual transformer models for cross-lingual information processing. The workflow can be extended to support additional languages, multilingual content delivery, and broader NLP applications involving language understanding and translation.

---

# Limitations

* Translation quality depends on the pretrained model.
* No domain-specific fine-tuning was performed.
* Financial terminology may not always be translated optimally.
* Translation quality has not been formally evaluated using automated metrics.

---

# Future Work

* Support additional Indian languages
* Integrate sentiment analysis
* Add topic classification
* Perform translation quality evaluation
* Develop a Streamlit-based web interface
* Explore domain-specific model fine-tuning

---

# Reproducibility

This project promotes reproducibility through:

* Open-source implementation
* Fixed dependency versions
* Publicly accessible APIs
* Modular architecture
* Deterministic processing workflow

---

# Disclaimer

This project is intended for educational, research, and demonstration purposes. Translation quality may vary depending on article complexity and model limitations.

---

# Citation

If you use this project, please cite:

**Azhar, A. B. (2026). NewsTranslate-AI: Multilingual Business News Translation Pipeline Using mBART. GitHub Repository.**
