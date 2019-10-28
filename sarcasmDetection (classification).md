## sarcasmDetection (classification)

1. TfidfVectorizer进行特征表示，原始数据集中截取1500个样本$3:2$的比例划分训练集和验证集

   均为3188维，n-gram设定范围(1,3)对应unigram, bi-gram,tri-gram

2. $Randomized\quad TruncatedSVD$  可以有效快速的处理scipy.sparse稀疏矩阵，进行降维

3. $StandardScalar$ 对每一维度的数据进行归一化

4. $GridSearchCV$ 自动网格搜索最优参数

5. 最优参数如下：

   

   <img src="C:\Users\54627\AppData\Roaming\Typora\typora-user-images\1572264359860.png" width="300px" />

   F1 score作为metric，validation上可以达到0.92

   $ps:$ 因为句子连续，ngram起了作用，没有去掉句子中的表情和符号
   
   $Towards\quad Multimodal\quad Sarcasm\quad Detection$加入了上下文语境context，主要将老友记作为sarcasm的数据进行标注，在复现代码的dataloader阶段，机器翻译对越南语处理遇到了小问题，似乎是word2vec阶段越南语无法tokenizer分词，打算换一个数据集用seq2seq再试试