# Text analysis on NeurIPS papers

**Aim:** Perform text modelling and clustering on text from the Proceedings of the Neural Information Processing Systems (NeurIPS).

## ☑️ What did I do?
- _First_, I processed the full-text using Regex to:
  - Extract the abstract from the full-text by analyzing the various patterns the authors use in numbering and/or naming the sections following the abstract.
  - Remove the information after the acknowledgments and/or reference sections. Some reasons for doing so:
    * they are not actually a part of the full text; and
    * they must not have an undue influence on our text analysis.
  - Perform 3 rounds of text cleaning, the last one being lemmatization. For this, I compared the results from NLTK and Spacy, and I found that NLTK gave better results for the given data set.  
- _Secondly_, I performed Exploratory Data analysis on the number of words and characters in the title and abstract of the papers. I also gained insight into the words commonly used in them.
- _Lastly_, I trained a Gensim LDA model for topic modelling and used K-Means to perform clustering on the documents.

## 🔖 What I hope to do next
- I want to use [pywsd](https://github.com/alvations/pywsd) instead of NLTK for lemmatization and compare the results.
- I want to try other topic modelling techniques like LSA, NMF and the like. See [here](https://iq.opengenus.org/topic-modelling-techniques/).
***
S.D.G.
