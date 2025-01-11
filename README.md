

# Hierarchical and Multi-Model Approaches for Abstractive Summarization of News Articles

This repository contains the implementation of three abstractive summarization techniques described in the research paper *"Hierarchical and Multi-Model Approaches for Abstractive Summarization of News Articles: An In-Depth Comparative Analysis"*. Each technique is implemented in a separate file to facilitate understanding and usage.

## Overview

Summarization techniques included:
1. **Direct Summarization Using BART** (`bart_summarization.py`)
2. **Summarization Enhanced by Sentiment Analysis and Topic Modeling** (`sentiment_topic_modeling.py`)
3. **Hierarchical Summarization Strategy** (`hierarchical_summarization.py`)

These methods were rigorously tested on diverse datasets and evaluated using metrics like **ROUGE** and **BLEU**.

## Project Structure

- **`bart_summarization.py`**: Implements a straightforward pipeline using the BART model.
- **`sentiment_topic_modeling.py`**: Enhances summarization with sentiment analysis and topic modeling.
- **`hierarchical_summarization.py`**: Utilizes a hierarchical approach to handle long-form articles.
- **`evaluation.py`**: Evaluates the summarization models using ROUGE and BLEU metrics.

## Installation

1. Clone this repository:
   ```bash
   git clone https://github.com/yourusername/abstractive-summarization.git
   cd abstractive-summarization
   ```

2. Install the required Python packages:
   ```bash
   pip install -r requirements.txt
   ```

Ensure you have internet access to download pre-trained models and datasets used in the implementations.

## Usage

### 1. Direct Summarization Using BART

This model uses the BART transformer model for abstractive summarization.

Run the script:
```bash
python bart_summarization.py
```

**Features**:
- Preprocesses input text by removing special characters and truncating long texts.
- Summarizes using the Hugging Face `facebook/bart-large-cnn` model.

### 2. Summarization Enhanced by Sentiment Analysis and Topic Modeling

This model integrates sentiment analysis (using BERT) and topic modeling (using LDA) with BART.

Run the script:
```bash
python sentiment_topic_modeling.py
```

**Features**:
- Sentiment analysis captures emotional tone.
- Topic modeling identifies key themes using Latent Dirichlet Allocation (LDA).
- Produces a summary aligned with the sentiment and topics of the original text.

### 3. Hierarchical Summarization Model

This mode breaks long texts into chunks, summarizes each, and combines them for a refined output.

Run the script:
```bash
python hierarchical_summarization.py
```

**Features**:
- Segments input text into chunks of up to 1024 tokens.
- Summarizes each chunk using BART.
- Combines individual summaries into a final cohesive summary.

### 4. Evaluation

Evaluate the summarization outputs using `evaluation.py`.

Run the script:
```bash
python evaluation.py
```

**Metrics**:
- **ROUGE-1**, **ROUGE-2**, **ROUGE-L**: Measures overlap between generated and reference summaries.
- **BLEU**: Evaluates the quality of generated text.

## Visualizations

The script provides insights into:
- **Generated Summaries**: Visualizes summaries from all models.
- **Sentiment Scores**: Displays the sentiment distribution of each generated summary.

