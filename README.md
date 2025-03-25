# MathCorpus-AATA

### Abstract Algebra Corpora Collection

This directory is dedicated to collecting corpora from the book [*Abstract Algebra: Theory and Applications*](https://github.com/twjudson/aata) by Thomas W. Judson. The full text (2022 edition) is available in [PDF format](http://abstract.pugetsound.edu/download.html) and can be accessed under a license through [Thomas W. Judson's GitHub repository](https://github.com/twjudson/aata).

These corpora are gathered at the request of [Valeria de Paiva](https://vcvpaiva.github.io/) for use in experiments aimed at extracting mathematical concepts for the [Topos Institute](https://topos.institute/), in accordance with the **Job Description** below.


**Note**: Using spaCy in Python, this process successfully extracted the relevant statistics and CoNLL-style features.


---------------------
### Job description:

After collecting a book, the student should make a GitHub repo and then use `spacy’ (https://spacy.io/) (or a similar off-the-shelf tool) to process it, producing stats (the script for the stats is from https://github.com/UniversalDependencies/tools/blob/master/udlib.pm . It’s called conllu-stats.pl), like was done for the nLab in https://github.com/ToposInstitute/nlab-corpus and for an updated nLab in  https://github.com/ToposInstitute/nLab2024-corpus. A nice, short  (4 min) tutorial on spacy is presented in https://medium.com/@pankaj_pandey/harnessing-the-power-of-spacy-a-comprehensive-guide-to-natural-language-processing-ffa6b1e6ff44.

A description of a similar project, building up corpora and benchmarks for mathematical text can be seen in the project [Mathscope](http://www.jacobcollard.com/mathoscope/) (Parmesan was renamed) of Collard and de Paiva, which is particularly concerned with Category Theory. The project has one example of a book [“Basic Category Theory”](https://thorsonlinguistics.github.io/bct/#p1), by Tom Leinster, processed this way and can be found here: https://github.com/ToposInstitute/CT-corpus/blob/main/bct.conll. 
As an illustration sentence 33 of the book looks like the following:

#sent_id = 33

#text = In subjects such as number theory and combinatorics, some questions are simple to state but extremely hard to answer.

| Token ID | Token        | Lemma         | Part of Speech (POS) | Morphological Tag | Morphological Features              | Head ID | Dependency Relation | Space Info       |
|----------|--------------|---------------|-----------------------|--------------------|--------------------------------------|---------|----------------------|------------------|
| 1        | In           | in            | ADP                  | IN                 | _                                    | 13      | prep                | _                |
| 2        | subjects     | subject       | NOUN                 | NNS                | Number=Plur                          | 1       | pobj                | _                |
| 3        | such         | such          | ADJ                  | JJ                 | Degree=Pos                           | 4       | amod                | _                |
| 4        | as           | as            | ADP                  | IN                 | _                                    | 2       | prep                | SpaceAfter=No    |
| 5        | \n           | \n            | SPACE                | _SP                | _                                    | 7       | dep                 | SpaceAfter=No    |
| 6        | number       | number        | NOUN                 | NN                 | Number=Sing                          | 7       | compound            | _                |
| 7        | theory       | theory        | NOUN                 | NN                 | Number=Sing                          | 4       | pobj                | _                |
| 8        | and          | and           | CCONJ                | CC                 | ConjType=Cmp                         | 7       | cc                  | _                |
| 9        | combinatorics | combinatoric | NOUN                 | NNS                | Number=Plur                          | 7       | conj                | SpaceAfter=No    |
| 10       | ,            | ,             | PUNCT                | ,                  | PunctType=Comm                       | 13      | punct               | _                |
| 11       | some         | some          | DET                  | DT                 | _                                    | 12      | det                 | _                |
| 12       | questions    | question      | NOUN                 | NNS                | Number=Plur                          | 13      | nsubj               | _                |
| 13       | are          | be            | AUX                  | VBP                | Mood=Ind|Tense=Pres|VerbForm=Fin     | 0       | ROOT                | _                |
| 14       | simple       | simple        | ADJ                  | JJ                 | Degree=Pos                           | 13      | acomp               | _                |
| 15       | to           | to            | PART                 | TO                 | _                                    | 16      | aux                 | _                |
| 16       | state        | state         | VERB                 | VB                 | VerbForm=Inf                         | 14      | xcomp               | _                |
| 17       | but          | but           | CCONJ                | CC                 | ConjType=Cmp                         | 14      | cc                  | SpaceAfter=No    |
| 18       | \n           | \n            | SPACE                | _SP                | _                                    | 20      | dep                 | SpaceAfter=No    |
| 19       | extremely    | extremely     | ADV                  | RB                 | _                                    | 20      | advmod              | _                |
| 20       | hard         | hard          | ADJ                  | JJ                 | Degree=Pos                           | 14      | conj                | _                |
| 21       | to           | to            | PART                 | TO                 | _                                    | 22      | aux                 | _                |
| 22       | answer       | answer        | VERB                 | VB                 | VerbForm=Inf                         | 20      | xcomp               | SpaceAfter=No    |
| 23       | .            | .             | PUNCT                | .                  | PunctType=Peri                       | 13      | punct               | _                |


We want statistics of the corpus, done for each book, so we can create a (somewhat) verified big corpus of mathematical texts.

