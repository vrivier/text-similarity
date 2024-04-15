# sentence-relatedness
Sentence relatedness using GloVe and LSTM on pytorch.  

#### Data
The dataset used for this project is the SICK dataset (Sentences Involving Compositional Knowledge, by Marelli et al.).  

#### Process
Sentence words are turned into vectors using GloVe word embeddings.  
They are then turned into 2 single vectors using pytorch LSTM.  
Finally these 2 vectors are merged by multiplication and substraction.  
The resulting vectors go through additionnal weight layers before a sigmoid function gives a similarity score between 0 and 1. 
