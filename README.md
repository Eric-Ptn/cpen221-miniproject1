# RateMyProfessor Sentiment Analysis + Synonym Prediction Model

This project involved a lot of separate tasks, but this is the most interesting stuff:

__SentimentAnalyzer__ in the `cpen221.mp1.sentimentanalysis` package: 
 - Given a review, a Bayesian probability is calculated with existing review data to determine the ratings associated with each word used in the review.
 - Laplacian smoothing was used to solve the problem of new words being introduced.
  
__MeaningFinder__ in `cpen221.mp1.sentimentanalysis.meaningfinder`:
 - Given a word and a list of other candidate words, finds the best synonym in the list for the given word by comparing the cosine similarities of the candidates with the given word.
 - The cosine similarity is computed with "marker vectors" for each word, which are formed by measuring the occurences of other words being used in the same sentence. The idea is that if two words are used in very similar contexts, they are likely similar in meaning.
 - The model is trained on a variety of texts from Project Gutenburg, as well as the __bee movie script__.
