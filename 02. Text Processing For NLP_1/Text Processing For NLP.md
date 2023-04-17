<a id="readme-top"></a>
<h1 align="center">Text Processing For NLP</h1>
<p align="center"> 
  <img src="/23 July'23 Text Processing For NLP/snapshots/txt_preprocess.jpg" width="350"alt="Text Processing" >
</p>

<!-- TABLE OF CONTENTS -->
<h2 id="table-of-contents"> Table of Contents</h2>

<details open="open">
  <summary>Table of Contents</summary>
  <ol>
    <li><a href="#txt_clean"> ➤ Text cleaning</a></li>
    <li><a href="#Tokenization"> ➤ Tokenization </a></li>
    <li><a href="#Stemming"> ➤ Stemming</a></li>
    <li><a href="#Lemmatization"> ➤ Lemmatization</a></li>
    <li><a href="#diff"> ➤ Stemming vs Lemmatization</a></li>
    <li><a href="#part"> ➤ Part-of-speech tagging </a></li>
    <li><a href="#ner"> ➤ Named entity recognition</a></li>
  </ol>
</details>

![-----------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)


<h2 id="txt_clean"> Text cleaning</h2>

<p align="justify"> 
  This involves removing unwanted characters, symbols, and words from the text data, such as punctuation, special characters, numbers, and stop words
</p>

<p align="center"> 
  <img src="/23 July'23 Text Processing For NLP/snapshots/text_clean.png" alt="linguistic Logo" >
</p>

<p align="justify"> 
  Computational Linguistics involves developing algorithms and techniques that allows computer to understand,generate and process human language. 

##### Uses below techniques to clean textual data

* Make all characters into lowercase
* Remove punctuation
* Remove numbers
* Remove Emojis
* Strip HTML Tags
* Remove URLs, Mentions (@), hastags (#) and special characters
* Remove stop words

</p>
<p align="right">(<a href="#readme-top">back to top</a>)</p>

![-----------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)


<h2 id="Tokenization"> Tokenization </h2>

<p align="center"> 
  <img src="/23 July'23 Text Processing For NLP/snapshots/token.png" alt="linguistic Logo" >
</p>

<p align="justify"> 

 * This involves breaking up the text into individual words or tokens. 
 * Tokenization is often the first step in many NLP tasks, as it allows the text to be analyzed on a word-by-word basis.
</p>
<p align="right">(<a href="#readme-top">back to top</a>)</p>

![-----------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)


<h2 id="Stemming">  Stemming </h2>
<p align="center"> 
  <img src="/23 July'23 Text Processing For NLP/snapshots/stemming.png" alt="linguistic Logo" >
</p>
<p align="justify"> 

 *  This involves reducing words to their root form, such as converting "running" and "ran" to "run". 
 * Stemming can help to reduce the number of unique words in a text corpus, making it easier to analyze.
</p>

<h4 id="uses" align="center"> Types of Stemming</h4>

<p align="center">There are several types of stemming algorithms used in NLP, including</p>

<p align="center"> 
  <img src="/23 July'23 Text Processing For NLP/snapshots/types_stemming.png" alt="linguistic Logo" >
</p>

1. <b>Porter stemming</b>
    + `This is one of the most widely used stemming algorithms in NLP`
    +  `It was developed by Martin Porter in 1979 `
    +  `based on a set of heuristic rules that remove common suffixes from words, such as "-ing" and "-ly"`
    +  `Porter stemming is simple and fast`.
  
2. <b>Snowball  stemming</b>
    + `This is an extension of the Porter stemming algorithm`
    +  ` It includes additional rules for stemming words in different languages, including French, German, and Spanish `
    +  ` Snowball stemming is more accurate than Porter stemming`
    +  `It is slower and more complex`
  
3. <b>Lancaster  stemming</b>
    + ` This is a highly aggressive stemming algorithm `
    +  `  Lancaster stemming is very fast and produces very aggressive stems, but it may produce stems that are not actual words `
  
</p>
<p align="right">(<a href="#readme-top">back to top</a>)</p>

![-----------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)


<h2 id="Lemmatization">  Lemmatization </h2>
<p align="center"> 
  <img src="/23 July'23 Text Processing For NLP/snapshots/lemma.jpeg" alt="linguistic Logo" >
</p>
<p align="justify"> 

 *  Lemmatization is the process of reducing a word to its base or root form, also known as a lemma.
 *  The purpose of lemmatization is to normalize words that have the same or similar meaning into a common base form, which makes it easier to analyze and compare them
 *  Lemmatization involves identifying the part of speech of a word and then applying morphological analysis to determine its base form.
 *  For example, the lemma of the word "running" would be "run", while the lemma of the word "walked" would be "walk".
</p>

<h4  align="center"> Applications  of Lemmatization </h4>

 + `Information Retrieval`
 +  `Sentiment Analysis `
 +  `Machine Translation.`
 +  `It is also used in search engines, where different variations of a word (e.g., "run", "runs", "running") are reduced to a common base form to improve search results.`
  
 <p align="right">(<a href="#readme-top">back to top</a>)</p>

![-----------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)


<h2 id="diff">  Stemming Vs Lemmatization </h2>

<p align="center"> 
  <img src="/23 July'23 Text Processing For NLP/snapshots/diff.png" alt="linguistic Logo" >
</p>

<p align="right">(<a href="#readme-top">back to top</a>)</p>

![-----------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)

<h2 id="part">  Part-of-speech tagging (POS tagging)</h2>
<p align="center"> 
  <img src="/23 July'23 Text Processing For NLP/snapshots/pos.jpeg" alt="linguistic Logo" >
</p>
<p align="justify"> 

 *  The process of labeling the words in a text with their corresponding parts of speech.
 *  POS such as noun, verb, adjective, adverb, pronoun, preposition, conjunction, or interjection.
 *  It is a crucial step in NLP as it helps to identify the grammatical structure of a sentence, which is important for tasks such as parsing, machine translation, and text-to-speech conversion.
 *  POS tagging algorithms typically use statistical models or rule-based approaches to assign each word a part of speech tag based on its context and its relationship to neighboring words in a sentence.
  `Example = The cat sat on the mat`
  `POS tagger would assign the tag "DT" (determiner) to "The", "NN" (noun) to "cat" and "mat", "VBD" (verb, past tense) to "sat", and "IN" (preposition) to "on"`
</p>
 <p align="right">(<a href="#readme-top">back to top</a>)</p>


![-----------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)

<h2 id="ner">Named Entity Recognition (NER) </h2>
<p align="center"> 
  <img src="/23 July'23 Text Processing For NLP/snapshots/ner.png" alt="linguistic Logo" >
</p>
<p align="justify"> 

 *   The process of identifying and categorizing named entities in a text, such as people, organizations, locations, dates, and other types of entities. 
 *  NER is an important task in NLP because it helps to extract structured information from unstructured text data.
 * NER algorithms typically use machine learning models, such as Conditional Random Fields (CRF) or neural networks, to identify named entities based on their context and their relationship to other words in a sentence. 
 *  POS tagging algorithms typically use statistical models or rule-based approaches to assign each word a part of speech tag based on its context and its relationship to neighboring words in a sentence.
  `Example = "Apple is headquartered in Cupertino, California", `
  `NER system would recognize "Apple" as an organization and "Cupertino, California" as a location.****`
</p>
 <p align="right">(<a href="#readme-top">back to top</a>)</p>