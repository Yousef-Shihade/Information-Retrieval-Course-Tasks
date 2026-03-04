# Task 04: PPMI (Positive Pointwise Mutual Information) Matrix

## Overview
This project explores word associations within a Data Science vocabulary using **Positive Pointwise Mutual Information (PPMI)**. While simple co-occurrence counts favor high-frequency words (like "the" or "and"), PPMI effectively identifies meaningful semantic relationships between technical terms by normalizing their individual frequencies.



## Features
* **Co-occurrence Simulation:** Generates a synthetic co-occurrence matrix for 20 Data Science expressions (e.g., *gradient*, *neuralnetwork*, *overfitting*).
* **PMI Calculation:** Computes the Pointwise Mutual Information:
  $$PMI(w, c) = \log_2\left(\frac{P(w, c)}{P(w)P(c)}\right)$$
* **PPMI Transformation:** Applies the "Positive" constraint, where $PPMI = \max(PMI, 0)$, to handle cases where word pairs occur less than expected by chance (which usually leads to negative infinity in log scales).
* **Visualization:** Utilizes a `Seaborn` heatmap to visualize the semantic clusters and association strengths across the vocabulary.

## Technical Stack
* **NumPy:** Used for matrix probability calculations and transformations.
* **Pandas:** To manage the expression-labeled dataframes.
* **Matplotlib/Seaborn:** For generating the association heatmap.

## Author
**Yousef Shihade**
Information Retrieval Course | University of Haifa
