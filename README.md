# Quora-Insincere-Question-classifier.

Problem Statement:
An existential problem for any major website today is how to handle toxic and divisive content. Quora wants to tackle this problem head-on to keep their platform a place where users can feel safe sharing their knowledge with the world.
Quora is a platform that empowers people to learn from each other. On Quora, people can ask questions and connect with others who contribute unique insights and quality answers. A key challenge is to weed out insincere questions those founded upon false premises, or that intend to make a statement rather than look for helpful answers.

Approach:
The data given by quora has question_id, question_text and a binary target (1 for insincere otherwise 0). There are 1.31 million such questions in train dataset and 376k questions to be classified as test data. 
I have used following embedding: glove.840B.300d (Link - https://nlp.stanford.edu/projects/glove/) 
Since the training data has 1.31 million observations and target is binary, intuitavely neural network makes sense for such problem. In addition Neural network can outperform other ML models as the data is large enough for NN to learn and give better accuracy. 

RNNs Vs. LSTMs & GRUs:
Eventhough RNNs have feedback loop and retains memory, it can be difficult to train RNN which has long term temporal dependencies. This is because of the phenomena called vanishing gradient problem which, in nutshell, is decay of loss function exponentially with time. On the other hand LSTM has additional cells which retains information for longer period of time using set of gates. GRUs have simplified structure but don't have any additional memory cells. For question classification, long term temporal dependencies are essential. So I have opted for LSTM for this problem.

Word Embeddings VS Bag of Words:
The main idea behind using word embeddings is to maintain semantic relationships which means that words that have similar meaning will be closer. Another advantage of Embeddings is dimention reduction of vectorized space. The curse of dimentionality can induce high amount of redundant information hence useful information can be lost essentially lowering performance.

Results: The LSTM performed as per my expectations as I got accuracy of 95.77% on validation set.
