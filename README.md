# ShortChineseTextClassfication
##this is a toy of NLP.
In this project,I use several models such as Transformer,SimpleCNN,SimpleRNN.
When choose I use Word2vec(train from the small corpus and pre-trained from a big coupus) and Char level Embedding(after remove stop words)

## Conclusion
### Attention is all you need.

#### Word Level Embedding
##### Embedding from target corpus
the corpus is too tiny,so the word level embedding (trained by the target text) is too bad, in RNN, I get 10% accuracy which means the model learn nothing about the trainning data.
in RNN,it's just 50%. While the transformer model got 72%!

##### Embedding from Renmin Paper news
RNN,CNN and Transformer are not bad,both of their accuracy is about 75%, the transformer also perform better than others.

##### End to End model
use the embedding in the classfier,the model would adjust the embedding for the target,transformer is also the best.

#### Char Level Embedding
I do not use all of the char,after cutting by jieba,use join method,we get a seq,the spilt the seq to char by char,then feed into the model.just like the end to end model.
