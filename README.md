# Quora-Insincere-Question-classifier.

Problem Statement:
An existential problem for any major website today is how to handle toxic and divisive content. Quora wants to tackle this problem head-on to keep their platform a place where users can feel safe sharing their knowledge with the world.
Quora is a platform that empowers people to learn from each other. On Quora, people can ask questions and connect with others who contribute unique insights and quality answers. A key challenge is to weed out insincere questions those founded upon false premises, or that intend to make a statement rather than look for helpful answers.

Approach:
The data given by quora has question_id, question_text and a binary target (1 for insincere otherwise 0). There are 1.31 million such questions in train dataset and 376k questions to be classified as test data. 
I have used following embedding: glove.840B.300d (Link - https://nlp.stanford.edu/projects/glove/) 
Model selection:
Since the training data has 1.31 million observations and target is binary, intuitavely neural network makes sense for such problem. In addition Neural network can outperform other ML models as the data is large enough for NN to learn and give better accuracy. 

