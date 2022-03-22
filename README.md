# LexicalProcessing_Tokenisation

## Tokenization with NLTK
NLTK (natural language toolkit ) is a python library developed by Microsoft to aid in NLP.
Word_tokenize and sent_tokenize are very simple tokenizers available in NLTK

It basically returns the individual works from the string.

Sent_tokenize splits the string into multiple sentences. The sent_tokenizer is derived from PunktSentenceTokenizer class. The sent_tokenize uses the pre trained model from tokenizers/punkt/english.pickle. There are pre trained models for different languages that can be selected. The PunktSentenceTokenizer can be trained on our own data to make a custom sentence tokenizer.

custom_sent_tokenizer = PunktSentenceTokenizer(train_data)
There are some other special tokenizers such as Multi Word Expression tokenizer (MWETokenizer), Tweet Tokenizer.

### MWETokenizer 
The MWETokenizer takes a string which is already been divided into tokens and retokenizes it, merging multiword expressions into single token, by using lexicon of MWEs.
Consider the sentence “He completed the task in spite of all the hurdles faced”
This is tokenized as [‘He’, ‘completed’, ‘the’, ‘task’, ‘in’, ‘spite’, ‘of’, ‘all’, ‘the’, ‘hurdles’, ‘faced’]
If we add the ‘in spite of’ in the lexicon of the MWETokenizer, then when the above tokens are passed to MWETokenizer it will be tokenized as [‘He’, ‘completed’, ‘the’, ‘task’, ‘in spite of’, ‘all’, ‘the’, ‘hurdles’, ‘faced’]

### Tweet Tokenizer
The TweetTokenizer addresses the specific things for the tweets like handling emojis.

### RegexpTokenizer
This tokenizer splits the sentence into words based on regular expression. For example in the below example, the tokenizer forms the tokens out of money expressions and any other non-whitespace sequences.

### Tokenization with Textblob
Textblob is used for processing of text data and is a library in Python. Similar to other packages it provides APIs for sentiment analysis, parts of speech tagging, classification, translation and so on. Below is the code fragment to tokenize into sentence and words and you can notice in the output the emoji’s are removed from the punctuation.


