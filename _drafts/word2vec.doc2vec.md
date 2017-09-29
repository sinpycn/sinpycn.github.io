
# Sentence Classification and Understanding

针对句子的分类，理解的处理是自然语言处理领域中很重要的研究领域。
这里将介绍以下几种句子的分类方法：
1. Bag-of-words
2. Word2Vec
3. Doc2Vec


# Bag-of-words
Bag-of-words是对句子中单词的出现次数的向量表示。 比如说
{I, have, a, pen, I, have, an, apple}
通过使用Bag-of-words向量表示时， 单词的顺序为： 
I, have, a, pen, an, apple
对应的单词频度为：
[2,2,1,1,1,1]

Bag-of-words的优点： 简单易懂， 计算效率高。
Bag-of-words的缺点：
  a. 没有考虑单词的出现顺序， 只要使用了相同的单词，那么表达出来的向量就是一样的。
  b. 不能表达语义，比如，programming， python， plane 三个单词的距离是一样的。 （按语义理解，programming和python应该是相近的）

# Word2Vec







https://github.com/jhlau/doc2vec#model-hyper-parameter-explanation

http://www.davidsbatista.net/blog/2017/04/01/document_classification/

https://groups.google.com/forum/#!topic/gensim/bEskaT45fXQ


https://github.com/RaRe-Technologies/gensim/blob/develop/docs/notebooks/doc2vec-IMDB.ipynb


https://deepage.net/machine_learning/2017/01/08/doc2vec.html


https://deepage.net/machine_learning/2017/01/08/doc2vec.html
