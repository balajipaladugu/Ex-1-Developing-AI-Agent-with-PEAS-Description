# Ex-1-Developing-AI-Agent-with-PEAS-Description
### Name:
P VENKATA BALAJI

### Register Number:
2305001024

### Aim:
To find the PEAS description for the given AI problem and develop an AI agent
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

### SPAM MAIL
### Algorithm:
Step 1: Define a list of spam keywords (e.g., “lottery”, “win money”, “free”, “click here”).

Step 2: Take incoming email text as input.

Step 3: Scan for presence of spam keywords.

Step 4: If spam keywords found → classify as SPAM, else classify as NOT SPAM.

Step 5: Print result for each email.
### Program:
```
class SpamFilterAgent:

def __init__(self):

    # Simple spam keywords list
    
    self.spam_keywords = ["lottery", "win money", "free", "offer", "click here", "prize", "urgent"]
    

def classify_email(self, email_text):

    # Check if any spam keyword exists in the email
    
    for keyword in self.spam_keywords:
    
        if keyword.lower() in email_text.lower():
        
            return "SPAM"
            
    return "NOT SPAM"
#For example

agent = SpamFilterAgent()

emails = [

"Congratulations! You have won a lottery. Click here to claim your prize.",

"Dear user, your account statement is attached for reference.",

"Urgent offer!!! Win money now by signing up for free.",

"Meeting scheduled tomorrow at 10 AM. Please attend on time."
]

for i, email in enumerate(emails, start=1):

result = agent.classify_email(email)

print(f"Email {i}: {result}")
```
### Output:

<img width="668" height="113" alt="image" src="https://github.com/user-attachments/assets/2d8cf527-587b-4c29-b60f-3a2dd7069b67" />

### Result:
Thus,The program for spam mail filer was implement and excuted
