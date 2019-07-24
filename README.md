A simple self-learning bot. Implementation of a Retrieval based chatbot based on Python's NLTK library (Natural Language ToolKit).

According to Medium (https://medium.com/analytics-vidhya/building-a-simple-chatbot-in-python-using-nltk-7c8c8215ac6e):
The Self learning bots use some Machine Learning-based approaches and are definitely more efficient than rule-based bots. Two types: Retrieval Based or Generative

In retrieval-based models, a chatbot uses some heuristic to select a response from a library of predefined responses. The chatbot uses the message and context of conversation for selecting the best response from a predefined list of bot messages. The context can include a current position in the dialog tree, all previous messages in the conversation, previously saved variables (e.g. username). Heuristics for selecting a response can be engineered in many different ways, from rule-based if-else conditional logic to machine learning classifiers.

NLTK is required to make programs understand and work with human language.

Install NLTK - pip install nltk
import nltk and then run nltk.download() to download the NLTK packages

Issue with text data is that it's all text and ML needs some sort of numerical vector.
Hence before we start working with this, we need to pre process the text to make it usable.
Basic pre processing:
