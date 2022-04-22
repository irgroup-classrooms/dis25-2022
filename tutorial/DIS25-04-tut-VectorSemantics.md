# Tutorial 4: Vector Semantics - Gensim, SpaCy, Word2Vec and GloVe

After you have dealt with synsemantics in the last tutorial, this tutorial is dedicated to vector semantics. Instead of manually created synsemantic networks,  in which words are linked in relationships to another, vector semantics automatically form word map semantic relations derived from co-occurrences in corpora.

Fortunately, there are Python modules that greatly simplify working with word embeddings and also make it straightforward to obtain pre-trained models.
In this tutorial, you will work with Gensim, a Python library specifically
for working with semantic vectors (https://radimrehurek.com/gensim/index.html).

Work through the tasks in a Jupyter notebook.


## 1. Importing the modules and data
### a) Import NLP modules
Import pandas, Numpy, NLTK and RE as in the first tutorial.
Install via pip or conda Gensim (in your console). Then import Gensim, KeyedVectors from gensim.models and the gensim.downloader as follows:

```python
import gensim
from gensim.models import KeyedVectors
import gensim.downloader
```
### b) Downloading and setting up models
You have heard about different attributes and types of word vector models in the lecture, in this tutorial you will compare different models. Pre-trained models can be obtained in several ways:
They can be self-trained via custom corpora, obtained via vectors (for example, from https://github.com/stanfordnlp/GloVe ) and transformed into models in Gensim, or, most straightforwardly, retrieved directly via the pre-trained models natively supported by libraries like Gensim.

As a Glove model, we have already prepared for you the "Glove 6b 100" model from the source mentioned (https://th-koeln.sciebo.de/f/657059193, password is the name of this course, letters all capital, DI..5) . You only need to load it as a model via the "KeyedVectors" class in Gensim:

```python
glove_6b_100_model = KeyedVectors.load_word2vec_format("glove.6B.100d.w2vformat.txt6", binary=False)
```
Next, use the following command to get a list of all the models contained in Gensim output a list of all models contained in Gensim:

```python
print(list(gensim.downloader.info()["models"].keys()))
```

Load the "glove-twitter-100" model via "gensim.downloader.load()" as follows:
```python
glove_twitter100_vectors = gensim.downloader.load("glove-twitter-100")
```

**The process can take time and uses a lot of system memory, if you have problems, skip downloading the pre-trained model via Gensim!**

The last method to get vector models we would like to show you is to create a model over a corpus of texts. For example, proceed as follows:
```python
corpus = gensim.downloader.load('text8')
from gensim.models.word2vec import Word2Vec
word2vec = Word2Vec(corpus)
```
## 2. functions of Vector Semantics
You should now have between one and three different vector models loaded.
Many vector semantic operations can be applied via Gensim's Word2Vec module API (available HERE)). Don't be confused by the naming, the methods are generally applicable to vector models, not just Word2Vec.
### a) Find similar expressions.
By similar_by_word() method, determine the 10 most similar terms to the words "summer", "salad", and "python". Discuss in the group: what do you notice? Can you see any differences between the models based on larger corpora (glove.6b and glove twitter100) and the Word2Vec model you trained based on the 32MB corpus? How could the differences differences come about?
### b) Relational Similarity.
Vector semantic models can be used to infer analogies of the form "A relates to B as A* relates to ...?" as they exist in the information extracted from the corpus. Using the method most similar() (see Gensim Word2Vec module API linked in introduction to question 2), you can thus have "Paris-France+Italy" find "Rome", for example:

```python
print('glove: Paris - France + Italy: ', glove_6b_100_model.most_similar(positive=["paris", "italy"], negative=["france"], topn=3))
```

Using this method, bias contained in the corpus, more precisely the vector models, can be revealed. For dichotomous features like [man,woman] or [young,old], put one of each in "positive" and "negative". Find out what the models for "doctor+woman", "housewife+man" as well as "car+sea" contain as their three next associations, choosing meaningful negatives. Discuss as a group! Can you find any other relational symmetries?
(c) Bonus: (Sentence) Similarity.
The method "n_similarity([], [])" can be used to judge the similarity of two lists of tokens to each other. Can you think of a useful application example? Discuss and try!

## 3. Pre-trained German vector models and vector-similarity with SpaCy
### a) Import modules and data
As you have learned in the second tutorial, Spacy is a powerful tool, that often has accessible, powerful functionalities built in, including word vector embeddings. Download a large German model, for example in your jupyter notebook by entering with the following command:
```python
!python -m spacy download de_core_news_lg
```

Attention: You will probably have to restart your Jupyter kernel for your system to find the can find the model. Load the model in your notebook with 

```python
nlp = spacy.load('de_core_news_lg')
```
### b) Similarity with SpaCy

Using pandas read_csv(), load the list of single term suggestions.txt from the previous tutorial and save it as a dataframe. Add another column "city" in which you determine the similarity of the term (suggestion_ger) to the document "nlp("city")". Do the same for "politics" and "recreation" and store the similarities in meaningful the similarities in meaningful named columns. 
Find the similarity between two texts using the ".similarity" method:
```python
simil = nlp("text number one").similarity(nlp("text number two"))
```
Discuss:
What could you use the particular similarities for?
