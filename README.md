# Bag of Words Spam Detection

This implements a spam detection system using the Bag of Words model and Naive Bayes classification. It processes text messages and classifies them as either spam or real (ham) messages.

## Requirements

```
numpy
pandas
matplotlib
nltk
scikit-learn
wordcloud
```

## Installation

1. Clone this repository:

```bash
git clone
cd bag-of-words-spam-model
```

2. Install the required packages:

```bash
pip install numpy pandas matplotlib nltk scikit-learn wordcloud
```

3. Download the required NLTK data:

```python
import nltk
nltk.download('stopwords')
```

## Usage

1. Ensure your spam dataset (spam.csv) is in the project root directory
2. Run the spam_detection.py script:

```bash
python spam_detection.py
```

The script will:

- Load and preprocess the dataset
- Create a Bag of Words model
- Train a Naive Bayes classifier
- Display a word cloud of common spam words
- Show the model's accuracy and confusion matrix
- Provide a function to predict if new messages are spam

## Dataset Format

The dataset should be a CSV file with the following columns:

- v1: Label column (spam/ham)
- v2: Text message content

## Example Usage

```python
from spam_detection import predict_spam

message = "URGENT! You have won a free iPhone! Click here to claim your prize!"
result = predict_spam(message)
print(f"Is spam: {result['is_spam']}")
print(f"Confidence: {result['confidence']:.2%}")
```

## Performance

The model typically achieves accuracy around 85-90% on the test set. Actual performance may vary depending on the dataset and preprocessing parameters.
