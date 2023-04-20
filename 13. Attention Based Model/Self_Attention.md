<a id="readme-top"></a>
<p align="center"> 
  <img src="images/self_attn.jpg" alt="Sequence" >
</p>

![-----------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)

<a id="readme-top"></a>

<h2 id="intro">Introduction to Self Attention</h2>
<p align="justify"> 
 Self Attention also known as dot product attention. It allows a model to attend to different positions of its own input sequnce while processing it. 
</p>
<p align="justify"> 
   Self attention is widely used in models such as transformer, which has been higly successfull in tasks like machine translation, text generation and language understanding.
</p>

![-----------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)

<a id="readme-top"></a>

<h2 id="intro">Limitations and Challenges in Attention Mechanism</h2>
<p align="justify"> 
 1. Traditional attention mechanisms, such as additive attention or multiplicative attention, were designed to attend to different parts of an input sequence relative to a fixed context vector. 
  <p  align="center">These mechanisms typically use separate query and context vectors, where the query vector is generated based on the current hidden state of the decoder in a sequence-to-sequence model, and the context vector is computed as a weighted sum of the input sequence elements. This allows the model to focus on different parts of the input sequence during the decoding process.</p>
</p>

<p align="justify">
2. They may not capture long-range dependencies effectively, as they rely on fixed context vectors that are computed based on the current hidden state of the decoder.
</p>

<p>
3. They may suffer from computational inefficiency when processing long sequences, as the attention scores need to be computed for all pairs of query and context vectors, which can be computationally expensive.</p>

<p align='center'>
Self-attention, on the other hand, addresses these limitations by allowing the model to attend to different positions of its own input sequence without relying on fixed context vectors
</p>
<p align='center'>
In self-attention, the query, key, and value vectors are all derived from the same input sequence, which enables the model to dynamically weigh the importance of different positions in the input sequence based on their relevance to the current context.
</p>
<p align='center'>
This makes self-attention more capable of capturing long-range dependencies and relationships between distant elements in the input sequence, and it can be more computationally efficient as it allows for parallel processing.
</p>

<p align="right">(<a href="#readme-top">back to top</a>)</p>
   
![-----------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)

<h2 id="intro">How it works? </h2>

 <b> Step1 </b> :  The input sequence is transformed into 3 kinds of vector- query vectors , key vectors and value vectors.These vectors are actually abstractions that are useful for calculating and thinking about attention.

<b> Step2 </b> :  Calculate score. Suppose we wish to calculate score for first word of our input seq then we need to score each word of input sentence against this word.The score determines how much focus to place on other parts of the input sentence as we encode a word at a certain position

 + The score is calculated  by taking the <b>dot product of the query vector with the key vector</b> of the respective word we’re scoring.  
 + So if we’re processing the self-attention for the word in position #1, the first score would be the dot product of q1 and k1. The second score would be the dot product of q1 and k2

<b> Step3 </b> : Dividing score by 8. This leads to more stable gradients.

<b> Step4 </b> : Pass the result obtained from step 3 to a softmax function which is responsible to normalize the scores, So that they are all positive and add up to 1.

<b> Step5 </b> : Multiply each value vector by softmax score. The intuition here is to keep intact the values of the word(s) we want to focus on, and drown-out irrelevant words (by multiplying them by tiny numbers like 0.001, for example).

<b> Step6 </b> : Sum up the weighted value vectors.This produces the output of the self-attention layer at this position (for the first word).

The resulting vector is one we can send along to the feed-forward neural network. In the actual implementation, however, this calculation is done in matrix form for faster processing. 

<p align="right">(<a href="#readme-top">back to top</a>)</p>
