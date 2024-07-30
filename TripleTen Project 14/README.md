# Sentiment Analysis for Film Review Classification

**Project Overview**

This notebook presents a comprehensive analysis and implementation of a machine learning solution for automatic sentiment classification of film reviews. The project aims to develop a robust model capable of distinguishing between positive and negative reviews with high accuracy, as measured by the F1 score.

**Objectives**

1. Implement and evaluate multiple text classification models
2. Achieve a minimum F1 score of 0.85 on the test set
3. Analyze model performance and select the optimal solution

**Methodology**

Our approach encompasses the following key steps:

1. Data preprocessing and exploratory data analysis
2. Feature engineering, including TF-IDF vectorization
3. Model training and evaluation, utilizing:
   - Logistic Regression
   - LightGBM
   - BERT embeddings
4. Comparative analysis of model performance
5. Final model selection and validation on custom test cases

**Dataset**

We utilize the IMDB movie review dataset, which consists of labeled film reviews. The dataset is pre-split into training and testing sets, allowing for consistent evaluation across different models.

**Success Criteria**

The primary metric for success is the F1 score, with a target threshold of 0.85. Additional metrics such as accuracy, precision, and recall will be considered for a comprehensive evaluation of model performance.

This notebook documents the entire process, from initial data exploration to final model selection, providing a transparent and reproducible workflow for our sentiment analysis task.

# Conclusion

In this project, we developed and evaluated several models to automatically detect negative reviews for the Film Junky Union. Our goal was to train a model that could achieve an F1 score of at least 0.85. Here are our key findings:

1. **Model Performance**: 
   - All our main models (except the baseline) exceeded the required F1 score of 0.85 on the test set.
   - The best performing models were Model 1 (NLTK, TF-IDF, and Logistic Regression) and Model 3 (spaCy, TF-IDF, and Logistic Regression), both achieving an F1 score of 0.88 and ROC AUC of 0.95 on the test set.
   - Surprisingly, more complex models like BERT (Model 9) didn't outperform the simpler TF-IDF based models for this specific task.

2. **Feature Engineering**: 
   - TF-IDF vectorization proved to be highly effective for this task, providing a good balance between performance and computational efficiency.
   - The choice of preprocessing library (NLTK vs. spaCy) didn't significantly impact the results, suggesting that either approach is suitable for this task.

3. **Model Selection**: 
   - Logistic Regression performed consistently well across different feature sets, outperforming more complex algorithms like LGBMClassifier for this particular problem.
   - The simpler models (Models 1 and 3) not only met but exceeded the project requirements, indicating that for this task, increased model complexity doesn't necessarily lead to better performance.

4. **Generalization**: 
   - When tested on our custom reviews, all models showed consistent behavior in line with their training performance, demonstrating good generalization capabilities.
   - The models were able to capture nuanced sentiments in the custom reviews, correctly identifying positive and negative tones in most cases.

5. **Practical Implications**: 
   - For the Film Junky Union's review classification task, we recommend using either Model 1 or Model 3 (TF-IDF with Logistic Regression).
   - These models offer the best balance of performance, simplicity, and computational efficiency, making them ideal for practical implementation.

In conclusion, this project demonstrates that relatively simple, traditional NLP techniques can be highly effective for sentiment analysis tasks. While advanced techniques like BERT have their place, it's crucial to consider the specific requirements and constraints of each project. In this case, TF-IDF vectorization combined with Logistic Regression provides an excellent solution that meets and exceeds the Film Junky Union's needs for automated review classification.
