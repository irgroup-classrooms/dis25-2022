# Tutorial 2: Wordnet
(Syn-)Semantic networks like WordNet are important resources for NLP. In this tutorial you will use basic functionalities of WordNet and the German variant GermaNet. Use the documentation for WordNet (https://www.nltk.org/howto/wordnet.html) and GermaNet (https://germanetpy.readthedocs.io/en/latest/). If you get stuck with the API documentation, use other documentations (via google) and platforms like stackoverflow.com or tutorials.

## Task 1: Importing modules and data
### a) Import NLP modules
Import Pandas, Numpy, NLTK and RE as in the first tutorial and import WordNet (as wn) from nltk.corpus.
### b) Import of "Quality-of-Life Modules"
Many modules are not necessary, but make it easier to work with larger corpora. As in the first tutorial, import the method pandarallel (for parallelization in pandas) and initialize it with pandarallel.initialize(). You can now use parallel\_apply() instead of the pandas method apply() for parallelizable tasks.
### c) Importing the data
A data set on biased words (words that carry bias or unobjective value) is provided for the WordNet tutorial. Import the data frame "data.pkl" saved as a pickle. (import pickle and use the "load()" method!)
## Task 2: Synsets
Synsets are the meaning-distinguishable definitions of words or tokens. One application purpose is to extend the context to words with meaning equivalent words. For the given dataset, we would like to capture the synonyms to the biased words in the form of the lemmas to the associated synsets.
### a) Find synsets
Extract a list of the pairwise different biased words (column "Label_bias") from the dataset and store them in a separate list "b_words" (not in the dataframe!). 
### b) Find synonyms
For each of the words, determine all synsets and all lemmas belonging to the synsets. Store all pairwise different lemmas for all biased words in a list "b_words_synonyms". 
### c) Candidates for further biased words
The synonyms for the biased words that you have just determined are a good starting point for manually finding additional biased words. Finally, create a list "new_b_words" in which you store all words of the list "b_words_synonyms" that are not contained in the original list of "b_words". For all 3 generated lists, display the number of words contained.

# Part 2 GermaNet
GermaNet is the version of Germanet developed at the University of Tübingen for relational synsemantic word networks in German. Although the basic functionalities are largely identical to Wordnet, they are called differently. Since you will be dealing more with German datasets from the ESUPOL project later in this course, GermaNet could be a useful tool for semantic analysis.

### a) Install and import GermaNet
GermaNet is not in the public domain; the TH Köln has been granted a license for use in the context of teaching and research. Therefore, use GermaNet only for assignments and projects within the scope of this course. 
To gain access, you have to sign the non-disclosure agreement. If you have not done so in the lecture or did not recieve a mail with a link to the files, please fill in and sign the ([document](Classroom-Student-Germanet.pdf)) and mail it to fabian.haak@th-koeln.de. 
Copy the provided folder "germanetpy" into your site-packages folder, where your other installes python modules can be found. 
After that, make sure that germanet works properly. You can install the module via pip and make sure it is found by your system:

```python
import sys
!{sys.executable} -m pip install -U germanetpy
```

WordNet uses XML for relations and text files for frequencies, which must be stored in a specific location. Follow the instructions of the official API to set up GermaNet correctly:


```python
from pathlib import Path
from germanetpy.germanet import Germanet

data_path = str(Path.home()) + "/germanet/GN_V150/GN_V150_XML"
frequencylist_nouns = str(Path.home()) + "/germanet/GN_V150/FreqLists/noun_freqs_decow14_16.txt"
germanet = Germanet(data_path)
```
### b) Import data set
Import the file "single_term_suggestions.txt" as a dataframe. The file contains a list of single-word query suggestions from the 2017 federal election dataset presented in the lecture. You can use the Pandas method "read_csv".
## Task 4: Using Germanet
### a) Synsets
Determine all synsets for each of the suggestions (i.e., each row of data) and store the list in a separate column.
### b) Lexical units
For each row, determine all lemmas (lexical units, i.e. lexunits) for all synsets and enter them as a list in a new column. 
### c) Hypernyms
Semantic networks such as Germanet describe actual relationships between synsets. Hypernyms (supertypes) and hyponyms (subtypes) can be useful for classifying terms.
Determine all hypernyms for all synsets of each suggestion and store their synsets in a column "hypernyms". Then determine the lemmas of these hypernyms and store them in a separate column. 
### d) Hyponyms
Proceed as in c, but this time determine the hyponyms of the suggestions and their lemmas. Find the number of all unique hypernyms, hyponyms and lemmas.
### BONUS TASK: Semantic Similarity and Relatedness
The relational structure of synsets can be used to infer the similarity or relatedness of two terms of the same word type. In turn, the similarity can be used, for example, to eliminate ambiguity. In the case of the dataset, the terms form search suggestions to person-related searches in search engines, which are based on the names of politicians as search terms. Thus, the term "abort" was suggested as a search suggestion for at least one politician's name. To identify the relevant synset from the suggestions, the similarity to the synset "politician" ( synset(id=s34818, lexunits=politician, politician) ) can be determined. 

Proceed as explained in the official GermaNet tutorial (https://github.com/Germanet-sfs/germanetTutorials/tree/master/pythonAPI) to calculate the similarity to the politician synset for all synsets of all suggestions, respectively, and store the synset with the highest similarity in a "best_syn" column. Use either Path- or IC- based similarity or run both separately. Finally, export a sub-dataframe containing only those rows whose suggestion has at least 2 synsets. 
