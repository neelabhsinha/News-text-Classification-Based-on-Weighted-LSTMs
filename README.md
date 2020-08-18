# News-text-Classification-Based-on-Weighted-LSTMs

This repository is an attempt to implement the technique used in the paper [W-RNN: News Text Classification based on a Weighted RNN](https://arxiv.org/ftp/arxiv/papers/1909/1909.13077.pdf), and then comparing it with tge results obtained with standard LSTM based and Bi-LSTM based techniques. Further, an **additional model is also proposed which improves the performance over the WRNN model**.

Dataset: [20 News Groups](http://qwone.com/~jason/20Newsgroups)

### Description of Files in this repository:

- Final_CODE.ipynb : Contains our source code   
- Generator.ipynb : Contains the code for word2vec and dataset generations     
- train_data.p : Training dataset after cleaning  
- desired_train_data.p : Training desired values  
- test_data.p : Testing dataset after cleaning  
- desired_test_data.p : Testing desired values 
- Predictions : The prediction list of 100 documents  
- wordvectors1.kv : word2vec generated keyed vectors 

### Steps to execute the code in this reposirory:

1. Install Anaconda Distribution and all relevant libraries

2. Open up the terminal and type -

``` cmd
$git clone https://github.com/neelabhsinha/News-text-Classification-Based-on-Weighted-LSTMs.git
$cd News-text-Classification-Based-on-Weighted-LSTMs
$jupyter notebook
```

### WRNN with LSTM Architecture -
<img src="/Graphs and Results/W-RNN/WRNN_Chart.png" width="550" height="500">

- Additional Model Proposed: Bidirectional WRNN (Replaces the LSTM unit with Bi-LSTM unit)

### Training -
(Shown for the WRNN model only) 

<img src="/Graphs and Results/W-RNN/WRNN_Graphs.png" alt="Training" style="width:100%">

### Additional Improvements done in the Architecture of the Model -
- Introduced Regularization and Recurrent Dropout in the LSTM unit
- Used Time Distributed Layers to weigh intermidiate output instead oc conv1d layer
- Used Dropout and L1, L2 architecture in Dense Layers

### Results -

S. No. | Model Name | Accuracy | F1-score (Obtained) | FI-score (as quoted in the paper) |
-------|------------|----------|----------| ----------------------------------|
1 | RNN (Baseline 1) | 67.8% | 64.5% | 78% |
2 | BiLSTM (Baseline 2) | 87.9% | 87.5 % | 75% |
3 | WRNN (Paper Model) | 89.5% | 88.8% | 84% |
4 | Bi-WRNN (Additional Model) | 89.2% | 88.7% | - |

- Significant Improvement over results quoted in the paper
- Additional Model works well
- The results improved due to better generalization in the model due to proper use of L1, L2 regularization, and Dropout


