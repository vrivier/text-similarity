# sentence-relatedness
Sentence relatedness using GloVe and LSTM on pytorch.  

#### Data
The dataset used for this project is the SICK dataset (Sentences Involving Compositional Knowledge, by Marelli et al.).  

Few examples : 

| id  | sentence 1          | sentence 2 | similarity score |
| --------------- |---------------| -----| ------ |
|2651| the man is slicing vegetables  |  there is no woman slicing a potato |  0.5 |
|2650| the man is slicing vegetables    |   a woman is cutting a potato |  0.6 |
|3985| a tomato is being sliced by a woman    |   a woman is peeling a potato |  0.66 |

#### Process
Sentence words are turned into vectors using GloVe word embeddings.  
They are then turned into 2 single vectors using pytorch LSTM.  
Finally these 2 vectors are compared using dot product and euclidian distance.  
The result goes through a sigmoid function that gives a similarity score between 0 and 1. 
