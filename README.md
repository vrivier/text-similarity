# Text similarity
Evaluating the semantic similarity between sentence pairs using GloVe and LSTM on pytorch.  

#### Data
The dataset used for this project is the SICK dataset (Sentences Involving Compositional Knowledge, by Marelli et al.).  

#### Process
1 - Words are turned into vectors using GloVe word embeddings.  
2 - Both sentences are turned into vectors using pytorch LSTM.  
3 - The 2 sentence vectors are merged by multiplication and substraction.  
4 - The resulting vectors go through additionnal weight layers.  
5 - A sigmoid function gives a similarity score between 0 and 1. 
