# Text analysis on NeurIPS papers

**Aim:** Perform text modelling and clustering on text from the Proceedings of the Neural Information Processing Systems (NeurIPS).

## ☑️ What did I do?
- _First_, I processed the full-text step by step to extract useful information; and remove unwanted information.
  - I extracted the abstract from the full-text by analyzing the various patterns that the authorsd use in numbering and/or naming the sections following the abstract.
  - Then, I removed the information after the acknowledgments and/or reference sections. Some reasons for doing so are that:
    * they are not actually a part of the full text;
    * they must not have an undue influence on our text analysis; and
    * frankly, I don't see much gain in saving that information in a new column for checking, maybe, which paper is referenced by which other paper.
  - After this, I used 3 rounds of text cleaning, the last one being lemmatization. For this, I compared the results from NLTK and Spacy, and I found that NLTK gave better results for the given data set.  
- _Secondly_, I performed Exploratory Data analysis on the number of words and characters in the title and abstract of the papers. I also gained a picture of the most common words used in the two.
- _Thirdly_, I trained a Gensim LDA model for topic modelling and explored:
    * the variation of dominant topics; and
    * the most frequent words in each topic.
- _Lastly_, I used K-Means to perform clustering on the documents.

## 🔖 What I hope to do next
- I want to use [pywsd](https://github.com/alvations/pywsd) instead of NLTK for lemmatization and compare the results.
- I want to try other topic modelling techniques like LSA, NMF and the like. See [here](https://iq.opengenus.org/topic-modelling-techniques/).
