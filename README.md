# Ex-1-Developing-AI-Agent-with-PEAS-Description
### Name:

### Register Number:

### Aim:

### Theory :
PEAS stands for:
'''
P-Performance measure

E-Environment

A-Actuators

S-Sensors
'''

It’s a framework used to define the task environment for an AI agent clearly.

### Pick an AI Problem

```

1. Self-driving car

2. Chess playing agent

3. Vacuum cleaning robot

4. Email spam filter

5. Personal assistant (like Siri or Alexa)
```

### VacuumCleanerAgent
### Algorithm:
Step 1: Prepare Dataset

Collect sample emails and their corresponding labels (spam or ham).

Step 2: Convert Text to Numeric Features

Use CountVectorizer to transform email text into a numeric feature vector.

Each unique word becomes a feature.

Each email is converted into a vector representing word counts.

Step 3: Train Classifier

Use Multinomial Naive Bayes to train on the numeric vectors and labels.

The model learns which words are likely associated with spam vs ham.

Step 4: Test New Email

Convert the new email into a numeric vector using the same CountVectorizer.

Use the trained Naive Bayes model to predict whether the new email is "spam" or "ham".

Step 5: 
Print the email content and predicted label.

### Program:
```
from sklearn.feature_extraction.text import CountVectorizer
from sklearn.naive_bayes import MultinomialNB
emails = [
    "Win money now!!!", 
    "Lowest price for medicines", 
    "Hi, how are you?", 
    "Meeting tomorrow at 10am", 
    "Congratulations, you won a lottery", 
    "Reminder: project submission"
]
labels = ["spam", "spam", "ham", "ham", "spam", "ham"]

vectorizer = CountVectorizer()
X = vectorizer.fit_transform(emails)

model = MultinomialNB()
model.fit(X, labels)

test_email = ["Get cheap loans now"]
test_vector = vectorizer.transform(test_email)
prediction = model.predict(test_vector)

print("Email:", test_email[0])
print("Prediction:", prediction[0])
```
### Sample Output:

<img width="364" height="72" alt="image" src="https://github.com/user-attachments/assets/73abb029-550c-4b18-b7f5-e935c9b48108" />

### Result:
Thus,The program for spam mail filer was implement and excuted
