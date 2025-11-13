# Tfidf-customer-feedback-analysis
Customer feedback analysis (Text) analysis using TF-IDF vectorization and cosing similarity
# Customer Feedback Analysis using TF-IDF

## Description
This project analyzes customer feedback messages using TF-IDF (Term Frequency-Inverse Document Frequency) vectorization and cosine similarity to identify similar documents.

## Features
- Transform text corpus into TF-IDF document-term matrix
- Compute cosine similarity between all document pairs
- Identify the most similar documents in the corpus

## Requirements
```
scikit-learn
numpy
```

## Installation
```bash
pip install -r requirements.txt
```

## Usage
```bash
python feedback_analysis.py
```

## How It Works

### 1. TF-IDF Vectorization
The script uses TfidfVectorizer from scikit-learn to convert text documents into numerical vectors. Each term is weighted by:
- **Term Frequency (TF)**: How often a term appears in a document
- **Inverse Document Frequency (IDF)**: How unique a term is across all documents

### 2. Cosine Similarity
Computes the cosine of the angle between document vectors. Similarity ranges from:
- **0**: Completely dissimilar
- **1**: Identical documents

### 3. Similar Document Detection
Identifies the pair of documents with the highest cosine similarity score.

## Sample Input
```python
corpus = [
    "The delivery was fast and the product was excellent.",
    "Very poor packaging, but the delivery was quick.",
    "I love the quality of this product!",
    "Product was damaged, very disappointing experience.",
    "Excellent service and quick response from the team."
]
```

## Sample Output
```
======================================================================
PART (a): TF-IDF Vectorization
======================================================================

Document-Term Matrix Shape: (5, 23)
Number of documents: 5
Number of unique terms: 23

======================================================================
PART (b): Cosine Similarity Between All Document Pairs
======================================================================

Pairwise similarities:
Document 0 vs Document 1: 0.3590
Document 0 vs Document 2: 0.1952
Document 0 vs Document 3: 0.2481
...

======================================================================
PART (c): Two Most Similar Documents
======================================================================

The two most similar documents are:

Document 0: "The delivery was fast and the product was excellent."
Document 1: "Very poor packaging, but the delivery was quick."

Similarity Score: 0.3590
```

## Why These Documents Are Similar
Documents 0 and 1 share common themes:
- Both discuss **delivery** (using synonyms "fast" and "quick")
- Both mention the **product**
- Similar vocabulary despite different sentiments

## Technologies Used
- **Python 3.x**
- **scikit-learn**: For TF-IDF vectorization and cosine similarity
- **NumPy**: For numerical operations

## Applications
- Customer feedback clustering
- Document similarity search
- Content recommendation systems
- Duplicate detection
- Sentiment analysis preprocessing

## Author
Olayemi Olugosi

## License
MIT License

## Contributing
Pull requests are welcome! For major changes, please open an issue first to discuss what you would like to change.
