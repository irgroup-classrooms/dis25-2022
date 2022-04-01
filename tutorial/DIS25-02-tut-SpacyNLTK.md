# Tutorial 2: Basic NLP Pipeline - Spacy
The goal of the first tutorial is to create an NLP pipeline and get familiar with the common NLP modules. You will be able to handle most of the tasks with pandas as well as the nltk module, which are the basis for many NLP projects. Please use a (Jupyter) notebook for your code, for keeping things clean, performative and easy to annotate. Believe me, it's worth the extra effort!



## How to find Information
Since you will not directly be able to solve all tasks just from what we provide in the lectures, we will provide you with some relevant materials and online-tutorials. Don't worry if you cannot solve a task; ask in the GitHub discussion forum or wait until we talk about it in the tutorial session.

### Python 
If you need a little refreshment of your Python skills or want to quickly find well-structured information on certain aspects of Python, check out the tutorials and documentation on [W3 Schools](https://www.w3schools.com/python/default.asp). 

### Pandas 
Pandas is THE tool for tabular data in python. It comes with a lot of useful features, but is not always self-explanatory. However, there is an accelent [documentation](https://pandas.pydata.org/pandas-docs/stable/user_guide/index.html) and a superb [tutorial](https://www.w3schools.com/python/pandas/default.asp) on Pandas, and we reccomend to check both out, especially the first few lessens of the tutorial! 

### NLTK
NLTK, the natural language toolkit, as the name suggests, provides virtually everything you need for natural language processing in python. Although Spacy gets more popular quickly, NLTK is still the most used module for most preprocessing and analysis tasks. Find the documentation on the [official website](https://www.nltk.org/), but thanks to the popularity, almost every problem was already discussed and every question answered somewhere on the internet and almost always, a google search for a description of a problem or an error message leads to a solution. 


## Spacy

Spacy is the latest and "best" NLP Python Framework. However, it is even further away from "standard" python than NLTK. Luckily, there is a very good tutorial on [the official website](https://course.spacy.io/en), not far away from where you can find the [excellent documentation](https://spacy.io/api). We recommend the introduction chapters of the documentation and the first two chapters of the Tutorial.

## 1: Installation and Import
### 1.1 Installation and Import of NLP Modules

The first Task is the same as in the first tutorial:
Make sure that the required modules "pandas", "numpy", "nltk", "sklearn", "spacy" and "re" are imported and get the version numbers of the modules.

Hint: Use <code>! pip install NAMEOFMODULE</code> to run command line / shell commands from your python jupyter notebook and install modules without having to use your terminal. 

### 1.2 Import of "Quality-of-Life Modules"
Install "pandarallel". Import pandarallel's method "pandarallel" (for parallelization in pandas) and initialize it with pandarallel.initialize(). Consult pandarallel's documentation or google if you need help with using pandarallel.

## 2: Import Data
Again, we will work with the jokes dataset from the first tutorial.

Read in the attached .json files as pandas dataframes and merge them into a single dataframe. When doing so, make sure that the source of the data is preserved as a key.

## 3: Data Preprocessing
This time, we want to perform our preprocessing using Spacy. 

### 3.1 Prepare Spacy
Load a model/pipeline (find a fitting model [here](https://spacy.io/models)), it should be a "medium" sized model (size of models is usually noted at the end of the model name), to be sure that it includes all the functionality you need.


### 3.1 Clean up text
Prepare the data so that the "body" column contains the entire text of the joke and that no format tokens (e.g. "\n") are included. Use Spacy pattern matching, if possible!

### 3.2 Tokenization
Use Spacy to tokenize the jokes. Save the results in a column "spacy_tokens".

### 3.3 Stopword removal
Remove all English stopwords from the generated tokens. Use Spacy.

### 3.4 POS Tagging
Determine POS tags for the tokenized texts and store them in a "pos" column. Again, use Spacy.


### 3.5 Lemmatization
Lemmatize the tokens of the texts and store the specific lemmas in a column "lemmata". Use the Spacy Lemmatizer.

## 4: How was that?
What do you think? How was working with Spacy compared to working with NLTK? Prepare some thoughts to share in out tutorial!

## 5 Bonus

Play around with some more Spacy functionalties! Feel free to show us what you did in the tutorial!