# Text similarity
Evaluating the semantic similarity between sentence pairs using GloVe and LSTM on pytorch.  

#### Data
The dataset used for this project is the SICK dataset (Sentences Involving Compositional Knowledge, by Marelli et al.).  

#### Process
1 - Words are vectorized using GloVe word embeddings.  
2 - Both sentences are vectorized using pytorch LSTM.  
3 - The 2 sentence vectors are merged by multiplication and substraction.  
4 - The resulting vectors go through additionnal weight layers.  
5 - A sigmoid function gives a similarity score between 0 and 1. 

#### Note 
This notebook has been edited on a fixed kaggle environment. It is not reproducible as such on another platform such as Colab, for instance. Notably, the torchtext module has been removed in recent Pytorch versions. Adapting the notebook to recent versions has shown impossible, notably since it relied on the BucketIterator to process the sentence pairs simultaneously and no equivalent feature has been found in recent versions. 
