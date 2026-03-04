# Task 02: Okapi BM25 Ranking Implementation

## Overview
This task implements the **Okapi BM25** (Best Matching 25) ranking function. BM25 is a sophisticated ranking algorithm used by search engines to estimate the relevance of documents to a given search query. It improves upon basic TF-IDF by incorporating document length normalization and term frequency saturation.

## Parameters Used
In this implementation, the following standard constants were used:
* **$k_1 = 1.6$**: Controls the term frequency saturation.
* **$b = 0.75$**: Controls the degree of document length normalization.

## Features
* **Vocabulary Management:** Uses a defined set of 10 Information Retrieval terms.
* **Document Length Normalization:** Calculates $avgdl$ (average document length) to penalize or reward documents based on their length relative to the corpus.
* **IDF Calculation:** Implements the BM25-specific Inverse Document Frequency formula:
  $$\text{IDF}(q_i) = \ln\left(\frac{N - n(q_i) + 0.5}{n(q_i) + 0.5} + 1\right)$$
* **Scoring Matrix:** Generates a detailed breakdown of scores per term and per document using `pandas`.

## Example Scenario
The script processes 6 sample documents against a query (e.g., "information retrieval python ranking") and outputs a ranked list of documents based on their relevance scores.

## Author
**Yousef Shihade**
Information Retrieval Course | University of Haifa
