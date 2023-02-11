# Fake news detection using machine learning.

## Project description

Fake news and rumors are rampant on social media, and believing in them can cause significant harm. With the COVID-19 pandemic, social media has become the main instrument for sharing information about it, and along with it, the circulation of fake news. In this project we propose to detect fake news about COVID-19, using a combination of a transformer and classical machine learning algorithms with different features such as the text, the text sentiment, NER tags, POS tags, and so on. Finally, we thoroughly compare the results providing the accuracy, precision, recall, and F1-score metrics of all the systems.

## Paper

The paper is available as part of this repository

## Code

The code is available in a Jupyter Notebook


## Results

**Note**: Abbreviations of the systems: DT: Decision Tree, LR: Logistic Regression, SVM: Support Vector Machine, GDBT: Gradient Boosting, TC: RoBERTa+XLM-RoBERTa
+XLNet+DeBERT transformer combination with soft voting, BERT: BERT transformer, NB: Naive Bayes, MLP: Multilayer Perceptron, RF: Random Forest.

| Model       | Accuracy $\uparrow$ | Precision $\uparrow$ | Recall $\uparrow$ | F1-score $\uparrow$ |
|-------------|----------------------|----------------------|------------------|----------------------|
| DT (baseline)  | 85.37               | 85.47               | 85.37            | 85.39               |
| LR (baseline)  | 91.96               | 92.01               | 91.96            | 91.96               |
| SVM (baseline) | 93.32               | 93.33               | 93.32            | 93.32               |
| GDBT (baseline) | 86.96               | 87.24               | 86.96            | 86.96               |
| TC (baseline)   | 98.31               | 98.31               | 98.31            | 98.31               |
|-------------|----------------------|----------------------|------------------|----------------------|
| BERT    | 97.52               | 96.51               | 98.83            | 97.66               |
| NB      | 80.23               | 82.18               | 79.46            | 80.80               |
| MLP     | 87.26±0.0092        | 85.96±0.0138        | 90.46±0.0082     | 88.14±0.0076        |
| RF      | 92.75±0.0017        | 91.22±0.0023        | 95.31±0.0029     | 93.22±0.0016        |
| DT          | 86.68±0.0029        | 86.75±0.0027        | 88.00±0.0054     | 87.37±0.0030        |
|-------------|----------------------|----------------------|------------------|----------------------|
| NB + BERT   | 97.24               | 96.74               | 98.04            | 97.38               |
| MLP + BERT  | 96.75±0.0060        | 95.52±0.0079        | 98.40±0.0035     | 96.94±0.0056        |
| RF + BERT   | 97.80±0.0007        | 97.02±0.0013        | 98.82±0.0004     | 97.91±0.0007        |
| DT + BERT   | 97.93±0.0007        | 98.04±0.0009        | 98.00±0.0020     | 98.02 ±0.0007       |

Accuracy, Precision, Recall, and F1-score of all the models for the test dataset. The table shows the mean and the standard deviation (mean±standard deviation) after training the models 20 times.

