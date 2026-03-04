# Task 06: Information Retrieval on OCR-Noisy Text

## Overview
This project simulates a real-world Information Retrieval challenge: searching through documents that contain errors from **Optical Character Recognition (OCR)**. When physical documents are scanned, characters are often misread (e.g., "s" becomes "5" or "o" becomes "0"). This task demonstrates how **Character $n$-gram** indexing can provide a "fuzzy match" that remains robust despite these errors.

## Features
* **OCR Noise Simulation:** A custom function that introduces synthetic errors into a corpus of 30 European city descriptions using substitution, deletion, and insertion rules.
* **Character $n$-gram Vectorization:** Instead of matching whole words, the system breaks text into 3-character sequences (trigrams). This allows the model to find similarities even if parts of a word are corrupted.
  * *Example:* "Paris" $\rightarrow$ `['par', 'ari', 'ris']`
* **Robust Retrieval:** Uses **TF-IDF** and **Cosine Similarity** to compare "clean" queries against "noisy" queries.
* **Performance Analysis:** Includes side-by-side bar charts and similarity tables to visualize how much OCR noise impacts search accuracy.

## Technical Tools
* **Scikit-learn:** Used for `TfidfVectorizer` (with `analyzer="char"`) and `cosine_similarity`.
* **Pandas & Matplotlib:** Used for data structuring and performance visualization.
* **Python (Random):** Used to create a stochastic noise model for character substitution.



## Results
The implementation shows that while OCR noise decreases the absolute cosine similarity scores, the character $n$-gram approach successfully retrieves the correct documents as the top results, proving its effectiveness for digitized historical archives.

## Author
**Yousef Shihade**
Information Retrieval Course | University of Haifa
