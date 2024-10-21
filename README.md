This project was a bachelor thesis aimed at automating the analysis of error logs from Boon Edam's Speedlane Compact systems using machine learning techniques. These systems generate extensive log data, and manually analyzing this information is challenging. By applying sequence classification methods, specifically Long Short-Term Memory (LSTM) networks and Conditional Random Fields (CRF), the goal was to identify and diagnose system errors more efficiently.

1.Data Preparation : 
Log data simplification: Removed irrelevant fields (e.g., node IDs) and focused on key attributes like error codes and failure descriptions.
Text summarization: Applied Natural Language Processing (NLP) techniques such as Term Frequency-Inverse Document Frequency (TF-IDF) and Latent Semantic Analysis (LSA) to summarize long descriptions and standardize the textual data.
Time windowing: Grouped events occurring within a 5-second window to form event sequences, as this was found to be the most suitable interval based on analysis of event frequency.

2.Model Implementation : 
LSTM Model:
- Used for analyzing sequential data and capturing temporal dependencies in error logs.
- The input consisted of sequences of error events combined with corresponding textual descriptions.
- Hyperparameters such as the number of layers, neurons per layer, optimizer, learning rate, and batch size were tuned to optimize model performance.
CRF Model:
- Designed to label sequences based on the relationships between event attributes.
- Utilized both observation-level and sequence-level feature functions to encode the characteristics of event sequences.
- Grid search was used to find the best hyperparameters, including regularization coefficients and the maximum number of iterations.

3.Evaluation
Metrics used: Accuracy, precision, recall, and F1-score were employed to evaluate model performance.
