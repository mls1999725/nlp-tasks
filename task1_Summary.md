# task1 Summary

### Classify the sentiment of sentences from the Rotten Tomatoes dataset

- 词袋模型(BOW)：用词频表示文本特征
- $$TF-IDF$$表示特征：每一个$word$用$TF (词频)\times IDF(逆文件频率)$ 表示
- 两种特征表示方法所求$Accuracy$相差不大
- 对$Sentiment$进行处理，变为二分类问题后，$validation$上的$Accuracy$明显大于多分类，后来觉得这样进行二分类没有意义。文本分类是通过文本中单词来进行分类，在电影评论情感分析中，0~4代表评论的褒性在增强，转化为二分类则没有实际意义。
- 用$LogisticRegression$作为分类器
- 最终用BOW表示文本特征，$4:1$划分验证集和训练集得到了0.63的$Accuracy$


