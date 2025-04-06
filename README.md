# Bag of Words Spam Detection

This implements a spam detection system using the Bag of Words model and Naive Bayes classification. It processes text messages and classifies them as either spam or real (ham) messages.

![image](https://github.com/user-attachments/assets/ffb5b76f-c79a-4347-9967-a09e524fdfbc)

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
git clone https://github.com/digitalRM/bag-of-words-spam-model.git
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

## Dataset Format

The dataset should be a CSV file with the following columns:

- v1: Label column (spam/ham)
- v2: Text message content

Data can be found [here.](https://github.com/nikitaa30/Spam-Filtering-techniques/blob/master/dataset%20for%20bag%20of%20words/spam.csv)

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
