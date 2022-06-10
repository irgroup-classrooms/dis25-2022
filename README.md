# Natural Language Processing (DIS25a/NLP)

This course can be taken for the Bachelor Programm Data and Information Science (DIS25a) or the Master Program Digital Sciences (NLP).

After easter all sessions are hosted at TH Köln, Claudiusstraße 1. The sessions will be held life. Slides will be usually available a night before the actual lecture. We try to record all lectures and tutorials for later referal (not sure how this works out with the sessions at Claudiusstraße).

## Schedule for Summer Semester 2022

(L) Lectures; (T) Tutorials; (P) Project

The first [lectures and tutorial were recorded and are available online](https://th-koeln.sciebo.de/s/Col70bcubHhymJx). The password is the same as for the Zoom sessions. 

| Date      | Slot 13:30h                              | Slot 15:15h                              | DIS25a (DIS B.Sc.) | NLP (DS M.Sc.) |
|-----------|------------------------------------------|------------------------------------------|--------------------|----------------|
| 1.4.2022  | [Introduction and Overview](slides/DIS25-01-Introduction.pdf) (L)            | [Basic Text Processing](slides/DIS25-02-BasicTextProcessing.pdf) (L)                | x                  | x              |
| 8.4.2022  | [Basic NLP Pipeline: NLTK](tutorial/DIS25-01-tut-basicPipeline.md) (T) [(solution)](tutorial/DIS25_1_solution.ipynb)              | [Common Toolkit: Spacy](tutorial/DIS25-02-tut-SpacyNLTK.md) (T) [(solution)](tutorial/DIS25_2_solution.ipynb)         | x                  | x              |
| 15.4.2022 | _no lecture_                             |                                          |                    |                |
| 22.4.2022 | [WordNet](slides/DIS25-03-WordNet.pdf) (L) | [Vector Semantics](slides/DIS25-04-VectorSemantics.pdf) (L)| x                  | x              |
| 29.4.2022 | [WordNet, GermaNet](tutorial/DIS25-03-tut-WordNet.md) (T) [(solution)](tutorial/DIS25_3_solution.ipynb)                  | [Vector Semantics](tutorial/DIS25-04-tut-VectorSemantics.md) (T)   [(solution)](tutorial/DIS25_4_solution.ipynb)                  | x                  | x              |
| 6.5.2022  | [Information Extraction](slides/DIS25-05-infoextract.pdf) (L)               | [Sentiment Analysis](slides/DIS25-06-sentimentAnalysis.pdf) (L)                   | x                  | x              |
| 13.5.2022 | _no lecture_                             |                                          |                    |                |
| 20.5.2022 | [Language Models and Ethics in NLP](slides/DIS25-07-LM-Ethics.pdf) (L)    | Group assignment (P)                     | x                  | x              |
| 27.5.2022 | Group work (P)                           | Group work (P)                           | x                  |                |
| 3.6.2022  | Data Programming for IE (L)              | Group work (P) / Oral Exam Master        | x                  | x              |
| 10.6.2022 | [Guest Lecture: Dimitar Dimitrov](data/guest_lecture.md)(L)                        | Group work (P)                           | x                  |                |
| 17.6.2022 | Group work (P)                           | Group work (P)                           | x                  |                |
| 24.6.2022 | [Student talks - Project presentation](presentations.md) (P) | Student talks - Project presentation (P) | x                  |                |
| 31.8.2022 | Submission of term papers                |                                          | x                  |                |

## Bachelor: Group Assignments

In the group assignments a group of four students has to work on a bias-related topic with a specific focus and on one of three datasets. In the group work phases starting on 20.5.2022 we will be available during the lecture time to help and advise. 

In the [presentations on 24.6.2022](presentations.md) you are expected to present a _concept_ regarding your specific topic and dataset. Please decribe the _motivation_, the _dataset_, your _methods_ and _NLP pipeline_, a _working prototype_ and some _first insights and results_.

The feedback gathered during the presentation should be used to write a final term paper on your specific topic and work. Please read the [guidelines for the term paper](term-paper.md). 

### Datasets 

Choose *one* of the following datasets to work on:

* [Bundestags Plenarprotokolle](https://www.bundestag.de/services/opendata)
* [Washington Post](https://github.com/irgroup/datasets/tree/master/WAPostv4) - Please sign [individual licence agreement](https://trec.nist.gov/data/wapost/Individual%20Application.pdf)
* One of the ESUPOL dataset, like [btw17](https://zenodo.org/record/1494858#.YoOgvS8Rpqs). You can find descriptions of the datasets [here](data/ESuPol_Datensätze_Übersicht.pdf)

### Topics

Choose *one* of the following topcis: 

#### Gender Bias

Gender bias is a group bias in which different genders are represented differently in terms of an aspect in a given (set of) document(s) than expected. Aspects for which there can be a bias range from quantitative measures (e.g., how many documents have male/female authors) to  more complex NLP measures (e.g., different sentiments in texts about male/female politicians or topical bias, different distributions of topics in texts geared towards male/female readers).

Examples for papers that investigate gender bias:

- [The Gender Gap Tracker: Using Natural Language Processing to measure gender bias in media](https://journals.plos.org/plosone/article?id=10.1371/journal.pone.0245533)

- [Does Gender Matter in the News? Detecting and Examining Gender Bias in News Articles](https://dl.acm.org/doi/10.1145/3442442.3452325)

- [Perception-Aware Bias Detection for Query Suggestions](https://link.springer.com/content/pdf/10.1007%2F978-3-030-78818-6.pdf)

#### Ethnic Bias

Like gender bias, ethnic or racial bias describes bias towards groups of people belonging to an ethnical (or religious) group. Ethnic bias includes harmful stereotypes and less blatant but still dangerous aspects like topical bias. Detecting ethnic bias is not only important because it may lead to even more severe instances of racism, and it is an infringement of the constitutional right to equal treatment.

Examples for papers that investigate ethnic bias:

- [Guilty by Association: Using Word Embeddings to Measure Ethnic Stereotypes in News Coverage](https://doi.org/10.1177/1077699020932304)

#### Non-Neutral Speech

Non-neutral language consists of many aspects of language that is subjective, opinionated, or otherwise implies valuation. This includes toxicity, ranging from forms of hate speech such as racism, incivility, profane, offensive and aggressive language to over-positive praises. Non-neutral language is especially problematic when it appears in types of documents that claim to be neutral, such as wikipedia or (public) news. A related concept is framing bias, defined as the use of subjective words or phrases linked with a particular opinion.

Examples for papers that investigate non-neutral language:

- [A Framework for the Computational Linguistic Analysis of Dehumanization](https://pubmed.ncbi.nlm.nih.gov/33733172/)

- [Linguistic Models for Analyzing and Detecting Biased Language](https://aclanthology.org/P13-1162.pdf)

#### Stance Detection

Stance is a concept that describes an opinion on a subject, most often in a political context. The goal of stance detection is to detect the stances of users/authors towards these subjects. Often, the subjects are known due to context (for example, abortion, weapon laws and gay marriage in political texts) or they have to be determined using approaches like entity recognition. A related concept is that of target-dependent or aspect-based sentiment analysis, in which the opinions on aspects (targets) are detected.

Examples for papers that investigate stance detection:

- [Stance and Sentiment in Tweets](https://dl.acm.org/doi/10.1145/3003433)

- [Political Ideology and Polarization of Policy Positions: A Multi-dimensional Approach](https://arxiv.org/abs/2106.14387)
