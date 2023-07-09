# Plagarism-Checker
Assignment for training
**Certainly! Let's go through the code and explain the theory behind it.**

The code you provided is a Python script that demonstrates how to preprocess text and check for word matches between a user prompt and website content. Here's a breakdown of the important parts:

**Importing necessary NLTK modules:**

nltk is the Natural Language Toolkit library, which provides various tools and resources for working with human language data.
stopwords from nltk.corpus contains a list of common words (e.g., "the," "is," "and") that are often removed from text as they don't contribute much to the overall meaning.
word_tokenize from nltk.tokenize is used to split text into individual words or tokens.
WordNetLemmatizer from nltk.stem is a tool for reducing words to their base or root form (e.g., "running" becomes "run").

**Downloading NLTK resources:**

The nltk.download function is used to download the necessary resources for tokenization, stopwords, and lemmatization. This step is required only once to ensure you have the required data.

**Preprocessing Text:**

The preprocess_text function takes a text input, tokenizes it into words, removes stop words, lemmatizes the remaining tokens, and then joins them back into a single string.
Tokenization is the process of splitting text into individual words or tokens. word_tokenize is used to perform tokenization.
Stop words are commonly occurring words that do not carry much information about the content of the text. The stopwords.words('english') returns a list of English stopwords, and the function removes these words from the tokenized text.
Lemmatization reduces words to their base or root form. The WordNetLemmatizer is used to lemmatize the tokens.
Finally, the preprocessed tokens are joined back into a single string using ' '.join(lemmatized_tokens).

**Checking for Word Matches:**

The check_word_match function takes a user prompt and website content as inputs and checks if any words in the prompt match with the words in the website content.
The prompt and website content are tokenized and preprocessed using similar steps as in the preprocess_text function.
The function then iterates through each word in the preprocessed prompt and checks if it exists in the preprocessed website content. If a match is found, the function returns True.
If no match is found for any word in the prompt, the function returns False.

**User Input and Website Content:**

The code prompts the user to enter a prompt using the input function and stores it in the prompt variable.
The website_content variable contains a sample text that represents the content of a website (e.g., obtained through web scraping).

**Performing the Word Match Check:**

The check_word_match function is called with the prompt and website_content as arguments to check if any words match.
The result is stored in the is_copied variable.

**Outputting the Result:**

Finally, the code checks the value of is_copied and prints an appropriate message based on the result.
The purpose of this code is to provide a simple demonstration of text preprocessing and word matching using NLTK. It can be used to check if a user prompt has any word matches with website content, which might suggest that the content has been copied or plagiarized.
