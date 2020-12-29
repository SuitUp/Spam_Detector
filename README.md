# -- author: @Vineet --

# Spam_Detector - Text Classification with Naive Bayes
A spam detection model trained on the Naive Bayes alogorithm, leveraging NLP to solve the problem of spam/ham in emails.


## About
The challenge of text classification is to attach labels to bodies of text, e.g., tax document, medical form, etc. based on the text itself!


## Dataset
Used the Enron email dataset for the model training. 
This is real email data from the Enron Corporation after the company collapsed.

Link to data-set :- http://www2.aueb.gr/users/ion/data/enron-spam/

Instructions :- download all of the numbered folders, i.e., enron1, enron2, etc., and put all of them inside a parent directory.


## Key Idea
let’s first understand the algorithm. 
For training,  we need three things: 
the (log) class priors, i.e., the probability that any given message is spam/ham; 
a vocabulary of words; 
and words frequency for spam and ham separately, i.e., the number of times a given word appears in a spam and ham message.

Given a list of input documents, we can write this algorithm :-
  1. Compute log class priors by counting how many messages are spam/ham, dividing by the total number of messages, and taking the log.
  2. For each (document, label) pair, tokenize the document into words.
  3. For each word, either add it to the vocabulary for spam/ham, if it isn’t already there, and update the number of counts. Also add that word to the global vocabulary.
