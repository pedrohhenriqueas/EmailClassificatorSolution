# Email Classifier: SPAM vs HAM 📧🤖

This project is an email classifier using the Naive Bayes algorithm to determine if an email is SPAM or HAM (non-SPAM). It uses the `scikit-learn` library to train a model based on features extracted from the email texts.

## Features ✨

- Loading and preprocessing an email dataset.
- Transforming text into vectors using the TF-IDF (Term Frequency-Inverse Document Frequency) method.
- Training a classification model using the Multinomial Naive Bayes algorithm.
- Evaluating the model's performance on training and testing datasets.
- Predicting whether new emails are SPAM or HAM.

## Technologies Used 💻

- **Python** 3.x
- **pandas**: Data manipulation.
- **scikit-learn**: Model creation and training.
  - `TfidfVectorizer`: Transformation of email texts.
  - `MultinomialNB`: Naive Bayes algorithm for classification.
- **NumPy**: Numerical operations and array manipulation.

## Installation ⚙️

1. Clone the repository to your local environment:
   ```bash
   git clone https://github.com/pedrohhenriqueas/EmailClassificatorSolution.git
   ```

2. Install the dependencies:
   ```bash
   pip install -r requirements.txt
   ```

## Dataset 📊

The dataset used in this project is the **SpamAssassin Public Corpus** (or any other dataset of your choice). The CSV file (`spam_assassin.csv`) should contain the following columns:
- `text`: The email text.
- `target`: The email classification, with 1 for SPAM and 0 for HAM.

## Execution 🚀

This project is structured as a Jupyter Notebook (`EmailClassificatorSolution.ipynb`). To run it:

1. Open the notebook in your Jupyter development environment, such as Jupyter Lab or Jupyter Notebook.
   
2. Execute the notebook cells to load the dataset, train the model, and make predictions for new emails.

## Sample Predictions 🔮

The notebook makes predictions for the following sample emails:

```python
new_emails = [
    "Exclusive offer just for you! Buy 1 get 1 free on all products. Hurry up!",
    "Dear friend, I hope you are doing well. Would love to catch up soon.",
    "Great news! You've been selected for an exclusive membership with benefits.",
    "Can we reschedule our meeting to next Wednesday? Let me know.",
    "Congratulations! You've won a gift card worth $1000. Click here to redeem.",
    "I wanted to thank you for your time during yesterday's meeting. Looking forward to working together.",
    "Get a free consultation on your tax filing. Book an appointment today.",
    "Important security update! Please verify your account to avoid suspension."
]
```

**Expected Output**:

```
Email: Exclusive offer just for you! Buy 1 get 1 free on all products. Hurry up!
Classification: SPAM

Email: Dear friend, I hope you are doing well. Would love to catch up soon.
Classification: HAM

Email: Great news! You've been selected for an exclusive membership with benefits.
Classification: HAM

Email: Can we reschedule our meeting to next Wednesday? Let me know.
Classification: HAM

Email: Congratulations! You've won a gift card worth $1000. Click here to redeem.
Classification: HAM

Email: I wanted to thank you for your time during yesterday's meeting. Looking forward to working together.
Classification: HAM

Email: Get a free consultation on your tax filing. Book an appointment today.
Classification: SPAM

Email: Important security update! Please verify your account to avoid suspension.
Classification: HAM
```

## Evaluation 📈

The model is evaluated using metrics such as accuracy, precision, recall, and F1-score. The model's performance on the training and testing sets is printed after execution.

**Accuracy on training set**: 94.25%  
**Accuracy on testing set**: 93.56%

## Contributions 🤝

Contributions to this project are welcome! Feel free to open issues and pull requests.

