# News-text-Classification-Based-on-Weighted-LSTMs

This repository is an attempt to implement the technique used in the paper [W-RNN: News Text Classification based on a Weighted RNN](https://arxiv.org/ftp/arxiv/papers/1909/1909.13077.pdf), and then comparing it with tge results obtained with standard LSTM based and Bi-LSTM based techniques. Further, an additional method is also proposed which improves the performance over the WRNN model.

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

## WRNN -
<img src="/Graphs and Results/WRNN/WRNN_Chart.png">

Obtained Results:
- Long Short-Term Memory Netwerk (LSTM RNN) | Accuracy: 82.2%   
- Bi-directional Long Short-Term Memory Netwerk (Bi-LSTM RNN) | Accuracy: 87.9%  
- Weighted RNN (W-RNN) | Accuracy: 89.0%  

We also developed a new algorithm here which combines the characteristics of both Bi-LSTM RNN and W-RNN and achieves a maximum test accuracy of 89.2%, a significant improvement over the maximum accuracy acheived in the paper (85.5%).  


