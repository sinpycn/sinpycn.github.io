
# Sentence Classification and Understanding

针对句子的分类，理解的处理是自然语言处理领域中很重要的研究领域。
这里将介绍以下几种句子的分类方法：
1. Bag-of-words
2. Word2Vec
3. Doc2Vec


### Bag-of-words
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

### Word2Vec

#### Word2Vec是什么
Word2Vec是单词的向量表示方法，对单词的表示，常见的是使用one-hot向量的方法。 
与one-hot vector相比Word2Vec可以表达单词的语义，以及其文法， 经过word2vec表示的单词，不在是一个单独的词，而是包含了上下文统计信息的一种向量表达。

比如， 根据{I, have, a, pen, I, have, an, apple}建立一个词表， 那么我们可以得到I, have, a, pen, an, apple
当我们对pen使用one-hot表示时，可以得到[0,0,0,1,0,0].
apple为[0,0,0,0,0,1]

这种表达的缺点是，当词表中增加新单词时， 向量的维数就要增加。 另外也无法表达单词与单词之间的相互关系（相似，反义词等等）。

Word embedding方法解决了以上的几种缺陷，它支持更复杂的表达， 并且可以支持演算处理。

Word embedding通常表达为一个固定维数的向量，比如200-1000维。 它不是简单的将单词映射为向量，而是通过复杂的演算来对单词进行编码。

### Word2Vec的加减运算










https://github.com/jhlau/doc2vec#model-hyper-parameter-explanation

http://www.davidsbatista.net/blog/2017/04/01/document_classification/

https://groups.google.com/forum/#!topic/gensim/bEskaT45fXQ


https://github.com/RaRe-Technologies/gensim/blob/develop/docs/notebooks/doc2vec-IMDB.ipynb


https://deepage.net/machine_learning/2017/01/08/doc2vec.html


https://deepage.net/machine_learning/2017/01/08/doc2vec.html
