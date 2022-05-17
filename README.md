# Natural Language Processing (DIS25a/NLP)

This course can be taken for the Bachelor Programm Data and Information Science (DIS25a) or the Master Program Digital Sciences (NLP).

After easter all sessions are hosted at TH Köln, Claudiusstraße 1. The sessions will be held life. Slides will be usually available a night before the actual lecture. We try to record all lectures and tutorials for later referal (not sure how this works out with the sessions at Claudiusstraße).

## Schedule for Sommer Semester 2022

(L) Lectures; (T) Tutorials; (P) Project

[Lectures and tutorial are recorded and available online](https://th-koeln.sciebo.de/s/Col70bcubHhymJx). The password is the same as for the Zoom sessions. 

| Date      | Slot 13:30h                              | Slot 15:15h                              | DIS25a (DIS B.Sc.) | NLP (DS M.Sc.) |
|-----------|------------------------------------------|------------------------------------------|--------------------|----------------|
| 1.4.2022  | [Introduction and Overview](slides/DIS25-01-Introduction.pdf) (L)            | [Basic Text Processing](slides/DIS25-02-BasicTextProcessing.pdf) (L)                | x                  | x              |
| 8.4.2022  | [Basic NLP Pipeline: NLTK](tutorial/DIS25-01-tut-basicPipeline.md) (T) [(solution)](tutorial/DIS25_1_solution.ipynb)              | [Common Toolkit: Spacy](tutorial/DIS25-02-tut-SpacyNLTK.md) (T) [(solution)](tutorial/DIS25_2_solution.ipynb)         | x                  | x              |
| 15.4.2022 | _no lecture_                             |                                          |                    |                |
| 22.4.2022 | [WordNet](slides/DIS25-03-WordNet.pdf) (L) | [Vector Semantics](slides/DIS25-04-VectorSemantics.pdf) (L)| x                  | x              |
| 29.4.2022 | [WordNet, GermaNet](tutorial/DIS25-03-tut-WordNet.md) (T) [(solution)](tutorial/DIS25_3_solution.ipynb)                  | [Vector Semantics](tutorial/DIS25-04-tut-VectorSemantics.md) (T)   [(solution)](tutorial/DIS25_4_solution.ipynb)                  | x                  | x              |
| 6.5.2022  | [Information Extraction](slides/DIS25-05-infoextract.pdf) (L)               | [Sentiment Analysis](slides/DIS25-06-sentimentAnalysis.pdf) (L)                   | x                  | x              |
| 13.5.2022 | _no lecture_                             |                                          |                    |                |
| 20.5.2022 | Language Models and Ethics in NLP (L)    | Group assignment (P)                     | x                  | x              |
| 27.5.2022 | Group work (P)                           | Group work (P)                           | x                  |                |
| 3.6.2022  | Data Programming for IE (L)              | Group work (P) / Oral Exam Master        | x                  | x              |
| 10.6.2022 | [Guest Lecture: Dimitar Dimitrov](data/guest_lecture.md)(L)                        | Group work (P)                           | x                  |                |
| 17.6.2022 | Group work (P)                           | Group work (P)                           | x                  |                |
| 24.6.2022 | Student talks - Project presentation (P) | Student talks - Project presentation (P) | x                  |                |
| 31.8.2022 | Submission of term papers                |                                          | x                  |                |

## Group Assignments

In the group assignments a group of four students has to work on a bias-related topic with a specific focus and on one of three datasets. In the group work phases starting on 20.5.2022 we will be available during the lecture time to help and advise. 

In the presentations on 24.6.2022 you are expected to present a concept regarding your specific topic and dataset. Please decribe the motivation, the dataset, your methods and NLP pipeline, a working prototype and some first insights and results.

### Datasets 

Choose *one* of the following datasets to work on:

* [Bundestags Plenarprotokolle](https://www.bundestag.de/services/opendata)
* [Washington Post](https://github.com/irgroup/datasets/tree/master/WAPostv4) - Please sign [individual licence agreement](https://trec.nist.gov/data/wapost/Individual%20Application.pdf)
* One of the ESUPOL dataset, like [btw17](https://zenodo.org/record/1494858#.YoOgvS8Rpqs). You can find descriptions of the datasets [here](data/ESuPol_Datensätze_Übersicht.pdf)

### Topics

Choose *one* of the following topcis: 

* Gender Bias

Gender bias is a group bias in which different genders are represented differently in terms of an aspect in a given (set of) document(s) than expected. Aspects for which there can be a bias range from quantitative measures (e.g., how many documents have male/female authors) to  more complex NLP measures (e.g., different sentiments in texts about male/female politicians or topical bias, different distributions of topics in texts geared towards male/female readers). 

* Ethnic Bias

Like gender bias, ethnic or racial bias describes bias towards groups of people belonging to an ethnical (or religious) group. Ethnic bias includes harmful stereotypes and less blatant but still dangerous aspects like topical bias. Detecting ethnic bias is not only important because it may lead to even more severe instances of racism, and it is an infringement of the constitutional right to equal treatment.

* Non-Neutral Speech

Non-neutral language consists of many aspects of language that is subjective, opinionated, or otherwise implies valuation. This includes toxicity, ranging from forms of hate speech such as racism, incivility, profane, offensive and aggressive language to over-positive praises. Non-neutral language is especially problematic when it appears in types of documents that claim to be neutral, such as wikipedia or (public) news. A related concept is framing bias, defined as the use of subjective words or phrases linked with a particular opinion.

* Stance Detection

Stance is a concept that describes an opinion on a subject, most often in a political context. The goal of stance detection is to detect the stances of users/authors towards these subjects. Often, the subjects are known due to context (for example, abortion, weapon laws and gay marriage in political texts) or they have to be determined using approaches like entity recognition. A related concept is that of target-dependent or aspect-based sentiment analysis, in which the opinions on aspects (targets) are detected.
