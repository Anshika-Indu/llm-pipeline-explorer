# LLM Pipeline Explorer

An interactive, browser-based educational tool that demonstrates how Large Language Models (LLMs) process text — from tokenization and vocabulary creation to embeddings, dimensionality reduction, and semantic similarity.

**Explore the pipeline. Understand the concepts. Visualize how language becomes numbers.**

## Overview

LLM Pipeline Explorer is a hands-on learning experience designed to make the foundational concepts behind Large Language Models easier to understand.

Instead of simply reading about tokenization or embeddings, users can experiment with their own text, inspect token IDs, visualize sentence embeddings in 3D, and compare how spelling-based and meaning-based representations behave.

The project runs directly in the browser using a single HTML file.

## Features

### 1. Tokenizer & Vocabulary Builder
- Build a vocabulary from a collection of training sentences.
- Convert text into lowercase tokens.
- Assign unique numerical IDs to vocabulary tokens.
- View token frequencies in a structured table.
- Handle unknown words using subword-style character splitting.

### 2. Interactive Tokenization
- Convert sentences into individual tokens.
- Visualize tokens as colour-coded chips.
- Associate each token with its vocabulary ID.
- Display tokenization statistics:
  - Number of characters
  - Number of tokens
  - Characters per token

### 3. Vocabulary Size Control
- Adjust vocabulary size using an interactive slider.
- Retain the most frequent words.
- Observe how reducing vocabulary size affects tokenization.
- See tokenization update dynamically.

### 4. 3D Sentence Embeddings
Explore how sentences can be represented as numerical vectors.

**Spelling-based embeddings**
- Generate character trigram representations.
- Hash trigrams into 64-dimensional vectors.
- Normalize vectors using L2 normalization.
- Reduce dimensions to 3D using a JavaScript implementation.

**Meaning-based embeddings**
- Generate semantic embeddings using Transformers.js.
- Model: `Xenova/all-MiniLM-L6-v2`.
- Compare semantic representations with spelling-based representations.

### 5. Interactive 3D Visualization
- Visualize sentence embeddings as points in 3D space.
- Explore sentence relationships visually.
- Hover over points to inspect complete sentences.
- Compare spelling-based and meaning-based representations.

### 6. Similarity Analysis
- Calculate cosine similarity between sentence vectors.
- Identify the five closest sentence pairs.
- Display similarity scores to three decimal places.

### 7. Custom Word & Sentence Explorer
- Enter your own words or sentences.
- Tokenize and generate embeddings.
- Add custom inputs to the existing 3D visualization.
- Highlight custom inputs using a distinct orange marker.
- Identify the three closest existing sentences.
- Inspect the first eight values of the generated embedding vector.

## Technologies Used

| Technology | Purpose |
|---|---|
| HTML5 | Page structure |
| CSS3 | Styling and layout |
| Vanilla JavaScript | Tokenization, vector generation and calculations |
| Plotly.js | Interactive 3D visualization |
| Transformers.js | Meaning-based embeddings |
| MiniLM-L6-v2 | Semantic feature extraction |

## Getting Started

### Run Locally

1. Clone the repository:

   ```bash
   git clone https://github.com/YOUR-USERNAME/YOUR-REPOSITORY.git
   ```

2. Navigate into the project directory:

   ```bash
   cd YOUR-REPOSITORY
   ```

3. Open `index.html` in your browser.

**Note:** Meaning-based embeddings require the page to be served over HTTP/HTTPS. Opening the HTML file directly using `file://` may prevent the model from loading.

### Run Using a Local Server

You can use Python's built-in HTTP server:

```bash
python3 -m http.server 8000
```

Open the following address in your browser:

```text
http://localhost:8000
```

Alternatively, access the deployed version through your hosting provider.

## Project Structure

```text
LLM-Pipeline-Explorer/
│
├── index.html      # Complete application
└── README.md       # Project documentation
```

All application code, including HTML, CSS and JavaScript, is contained in a single `index.html` file.

## Learning Objectives

This project explores several foundational concepts in Natural Language Processing (NLP) and LLM architecture:

- Vocabulary construction and token IDs
- Word and subword tokenization
- Unknown token handling
- Character n-gram representations
- Vector embeddings
- L2 normalization
- Dimensionality reduction
- Cosine similarity
- Semantic embeddings
- Differences between lexical and semantic similarity

## Important Notes

- Spelling-based embeddings are educational approximations, not embeddings produced by a trained language model.
- Meaning-based embeddings use a pretrained MiniLM model.
- The 3D visualization is a dimensionality-reduced representation. It does not preserve every relationship in the original high-dimensional space.
- Transformers.js downloads the required model when meaning-based mode is used for the first time.
- An internet connection is required for CDN dependencies and model downloads.

## Project Goal

The goal of LLM Pipeline Explorer is to make the internal text-processing concepts behind modern AI systems more tangible and approachable.

By experimenting with real text and visualizing numerical representations, learners can develop an intuitive understanding of how language is transformed into data that machine learning models can process.

---

**Built as a hands-on learning project exploring the fundamentals of LLMs, NLP and vector representations.**
