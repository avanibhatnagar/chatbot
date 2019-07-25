##Simple Retrieval Based Chatbot\
A simple self-learning bot. Implementation of a Retrieval based chatbot based on **Python's NLTK library** (Natural Language ToolKit).

According to Medium[1]:
The Self learning bots use some Machine Learning-based approaches and are definitely more efficient than rule-based bots. Two types: Retrieval Based or Generative

In retrieval-based models, a chatbot uses some heuristic to select a response from a library of predefined responses. The chatbot uses the message and context of conversation for selecting the best response from a predefined list of bot messages. The context can include a current position in the dialog tree, all previous messages in the conversation, previously saved variables (e.g. username). Heuristics for selecting a response can be engineered in many different ways, from rule-based if-else conditional logic to machine learning classifiers.

NLTK is required to make programs understand and work with human language.

Install NLTK:
```
pip install nltk
python
import nltk
nltk.download()
```
To import nltk and download the NLTK packages

Issue with text data is that it's all text and ML needs some sort of numerical vector.
Hence before we start working with this, we need to pre process the text to make it usable.
**Basic pre processing:**
1. converting to all uppercase or all lowercase to ensure uniformity so that all data is treated equally.
2. convert normal text strings into a list of tokens
  2a. Sentence tokenizer to find list of sentences.
  2b. Word tokenizer to find list of words in strings.

**After pre processing:**
Transform text to meaningful array of numbers so that it can be used in ML.

**Bag Of Words**
Describes occurrence of words within a document
Example from [1]:
If our dictionary contains the words {Learning, is, the, not, great}, and we want to vectorize the text “Learning is great”, we would have the following vector: (1, 1, 0, 0, 1).
Problem: highly frequent words start to dominate the document but may not have informational content.

**TF-IDF Approach**
To rescale frequency of words by how often they appear in all documents so that scores for words like "the" are also penalized [1]. This scoring approach is called Term Frequency - Inverse Document Frequency.

Here, Term Frequency: scoring of frequency of word in current document.
Inverse Document Frequency: scoring of how rare the word is across documents
*To implement Tf-IDF*
```
from sklearn.feature_extraction.text import TfidfVectorizer
```

**Cosine Similarity**
"TF-IDF is a transformation applied to texts to get two real-valued vectors in vector space. We can then obtain the Cosine similarity of any pair of vectors by taking their dot product and dividing that by the product of their norms. That yields the cosine of the angle between the vectors. Cosine similarity is a measure of similarity between two non-zero vectors [1]."

Cosine Similarity (d1, d2) =  Dot product(d1, d2) / ||d1|| * ||d2||

**Important libraries to import**
- nltk
- numpy as np
- random
- string

**Corpus** - collection of text to be used
The corpus used for this project can be found in the chatbot.txt file. You can change that to whatever you want.

**References**
[1] https://medium.com/analytics-vidhya/building-a-simple-chatbot-in-python-using-nltk-7c8c8215ac6e
