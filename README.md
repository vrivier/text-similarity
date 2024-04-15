# sentence-relatedness
Sentence relatedness using GloVe and LSTM on pytorch.  

#### Data
The dataset used for this project is the SICK dataset (Sentences Involving Compositional Knowledge, by Marelli et al.).  

The sentences are simple and the purpose of this project is to demonstrate a pytorch implementation of LSTMs and an example of text similarity evaluation. 

Few examples : 

| id  | sentence 1          | sentence 2 | similarity score |
| --------------- |---------------| -----| ------ |
|2651| the man is slicing vegetables  |  there is no woman slicing a potato |  0.5 |
|2650| the man is slicing vegetables    |   a woman is cutting a potato |  0.6 |
|3985| a tomato is being sliced by a woman    |   a woman is peeling a potato |  0.66 |

#### Process
1/ Words are turned into vectors using GloVe word embeddings.  
2/ Both sentences are turned into vectors using pytorch LSTM.  
3/ The 2 sentence vectors are merged by multiplication and substraction.  
4/ The resulting vectors go through additionnal weight layers.  
5/ A sigmoid function gives a similarity score between 0 and 1. 
