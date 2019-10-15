## Sentiment Analysis Using Deep Learning

- $RNN$循环神经网络的变体$LSTM$

- $torch.utils$库进行$dataloader$处理（$DataFrame$类型数据处理）

- 预处理：词频向量化，$TF-IDF$, 词汇表向量化

- $word\ tokenize$分词⇒词形还原⇒创建词汇表⇒用词汇表对句子进行向量化⇒手动pad处理⇒定义$LSTM$模型⇒$TensorDataset$和$DataLoader$⇒训练

- 词性还原的目的就是将长相不同，但是含义相同的词统一起来

- 分词也可以使用$split()$

- 定义$RNN$模型:

  - $word\ embedding$

  - $RNN$

  - $fc$

    

- $Accuray$

  - 未经过$clean$操作，未经过词形还原和去除非字母，小写化，为0.43$(word\ embedding)$
  - 经过$clean$操作，为0.574$(word\ embedding)$
  - 