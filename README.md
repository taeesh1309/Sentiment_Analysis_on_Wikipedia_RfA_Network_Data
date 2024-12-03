# Sentiment Analysis on Wikipedia RfA Network Data

## Overview
This project investigates the dynamics of the Request for Adminship (RfA) process on Wikipedia through sentiment analysis and network visualization. Using natural language processing techniques, the study categorizes voter comments as positive, negative, or neutral and explores their influence on the success of adminship requests.

## Key Features
- **Dataset**: The study utilizes the Wikipedia RfA network dataset from SNAP, containing structured (votes) and unstructured (comments) data.
- **Sentiment Analysis Approaches**:
  - **NER + Topic Modeling**: Combines Named Entity Recognition (NER) with Latent Dirichlet Allocation (LDA) to identify latent themes and semantic relationships in voter comments.
  - **Embeddings-Based Analysis**: Leverages pre-trained embeddings (GloVe and Word2Vec) for high-accuracy sentiment classification.
- **Baseline Comparison**:
  - **VADER**: Achieved an accuracy of 46.3%.
  - **TextBlob**: Achieved an accuracy of 46.9%.
  - **NER + Topic Modeling**: Accuracy ranged between 71.2% and 73.3%.
  - **Word2Vec**: Achieved a superior accuracy of 91.7%.
- **Visualization**: Interactive visualizations of voter-candidate networks to highlight sentiment distributions and community structures.

## Goals
1. Understand factors influencing the success of RfA requests.
2. Develop advanced models for sentiment analysis tailored to Wikipedia's unique context.
3. Provide actionable insights into improving the transparency and efficacy of the RfA process.

## Approach
### 1. Data Preprocessing
- Text cleaning (stop words, special characters).
- Vectorization using CountVectorizer for NER + LDA and word embeddings for the embeddings-based approach.

### 2. Sentiment Analysis Techniques
#### NER + Topic Modeling
- Integrates NER with LDA for feature extraction.
- Optimal topics identified using coherence scores.

#### Embeddings-Based Analysis
- GloVe and Word2Vec embeddings to capture semantic relationships.
- Word2Vec outperformed GloVe with an accuracy of 91.7%.

### 3. Visualization
- Analyzed sentiment distribution across voter-candidate networks.
- Enhanced interpretability through community detection and sentiment clustering.

## Results
| **Approach**            | **Accuracy** |
|--------------------------|--------------|
| VADER                   | 46.3%        |
| TextBlob                | 46.9%        |
| NER + Topic Modeling    | 71.2% - 73.3%|
| Word2Vec Embeddings     | **91.7%**    |

### Best Model Metrics (NER + Topic Modeling on 300 Rows)
| **Sentiment** | **Precision** | **Recall** | **F1-Score** |
|---------------|---------------|------------|--------------|
| Positive      | 91%           | 67%        | 77%          |
| Neutral       | 11%           | 69%        | 19%          |
| Negative      | 32%           | 31%        | 32%          |
| **Overall Accuracy** | **63%** |            |              |

## Future Work
1. Explore transformers (BERT, GPT) for nuanced sentiment analysis.
2. Include multilingual comments for a global perspective.
3. Incorporate temporal analysis to understand sentiment trends over time.
4. Develop interactive dashboards for real-time sentiment visualization.

## Visualization Examples
- Candidate-specific sentiment distribution.
- Overall voter-candidate network analysis.

## Authors
- **Taeesh Azal Assadi**  
  Virginia Polytechnic Institute and State University  
  Email: taeeshazalassadi@vt.edu  

- **Faraz Ulhaq Shah**  
  Virginia Polytechnic Institute and State University  
  Email: shahfaraz@vt.edu  

## References
Refer to the [report](Sentiment_Analysis_on_Wikipedia_RfA_Network_Data.pdf) for full implementation details, visualizations, and analysis.
