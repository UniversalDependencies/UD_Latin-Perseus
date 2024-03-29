# Summary

This Universal Dependencies Latin Treebank consists of an automatic
conversion of a selection of passages from the Ancient Greek and Latin
Dependency Treebank 2.1

# Introduction

The current UD treebank derives from texts taken from
the Ancient Greek and Latin Dependency Treebank 2.1 available at

* https://github.com/PerseusDL/treebank_data/tree/master/v2.1/Latin

The original data have been semi-automatically annotated. More precisely,
morphological annotation and lemmatization have been performed with the help of
the Morpheus morphological analyzer, while syntactic annotation has been done
manually. The following guidelines have been followed:

* http://nlp.perseus.tufts.edu/syntax/treebank/ldt/1.5/docs/guidelines.pdf

Further details can be found at:

* https://github.com/PerseusDL/treebank_data/tree/master/v2.1/Latin

This UD release contains parts of the following works:

| author | work |
| --- | --- |
| Augustus | Res Gestae |
| Cicero | In Catilinam |
| Jerome | Vulgata |
| Vergil | Aeneid |
| Ovid | Metamorphoses |
| Petronius | Satyricon |
| Phaerus | Fabulae |
| Propertius | Elegies |
| Sallust | Bellum Catilinae |
| Suetonius | Life of Augustus |
| Tacitus | Historiae |


# Acknowledgement

The current UD data have been converted by Giuseppe G. A. Celano.

The Ancient Greek and Latin treebank is a result of a joint effort between
Tufts University and Leipzig University (DH) under the supervision of Prof.
Gregory Crane. Current editors of the treebank are Giuseppe G. A. Celano,
Gregory Crane, and Bridget Almas.

Authors of the annotations are (in alphabetical order):

Giuseppe G. A. Celano, J. F. Gentile, Robert Gorman, Vanessa Gorman,
Jordan Hawkesworth, Yoana Ivanova, Tovah Keynton, Florin Leonte, Alex Lessie,
Daniel Lim Libatique, Meg Luthin, Francesco Mambrini, George Matthews,
Jack Mitchell, Molly Miller, Jessica Nord, Sean Stewart, Anthony D. Yates,
Polina Yordanova, and Sam Zukoff.

Further details can be found at:

* http://perseusdl.github.io/treebank_data/

# Basic statistics

Tree count:  2273
Word count:  29138
Token count: 29138
Dep. relations: 24 of which 0 language specific
POS tags: 12
Category=value feature pairs: 34

# References:

Bamman, David and Gregory Crane. 2011. The Ancient Greek and Latin Dependency
Treebanks. 2011. In Caroline Sporleder, Antal van den Bosch, Kalliopi Zervanou
(eds.), Language Technology for Cultural Heritage, 79-98.

Celano, Giuseppe G. A., Gregory Crane, and Bridget Almas. 2014.
The Ancient Greek and Latin Dependency treebank 2.0. https://github.com/PerseusDL/treebank_data

# Changelog

* 2023-11-15 v2.13
  * Orthographic univerbation of the conjunctional clitics *que* and *ue*, introducing multi-word tokens.

* 2023-05-15 v2.12
  * Introduced missing UPOS tags: DET for determiners, PART for particles; modified deprels accordingly (e.g., `det`). Generalised the use of PROPN for proper nouns, and AUX for auxiiaries (mostly *sum*); modified deprels accordingly (e.g. `flat`/`flat:name` for proper nouns).
  * Reannotated compound numerals (e.g. *viginti quattuor*) from `nummod` to `flat`.
  * Replaced `iobj` with `obl`/`obl:arg`.
  * Added `:relcl` subtype to `acl` relative clauses.
  * Added `:abs` subtype for so-called ablativus absolutus, now annotated as `advcl:abs`.
  * Replaced `parataxis` to `conj` when used for coordination.
  * Restored correct order of conjunctions *neque* and *nec*, previously found in the text as *que ne* and *c ne*.
  * Reattached conjunctions to the second conjunct instead of the first one.
  * Added `:neg` subtype for negations such as *non*, now annotated as `advmod:neg`.
  * Reannotated gerund and gerundive forms as participles (`VerbForm=Part`) with `Aspect=Prosp`, of supines as `VerbForm=Conv` with `Aspect=Prosp`; based on (Cecchini, 2021).
  * Sistematically added `PronType` to pronouns.
  * General improvement of morphological annotation. The following morphological features have been added if missing, corrected, or deleted if non relevant: `Aspect`, `Tense`, `Voice` for verbs; `Gender`; `Person` for pronouns.
  * Overall, implementation of syntactic and morphologic harmonisation interventions as described in (Gamba & Zeman 2023a) and (Gamba & Zeman 2023b).

* 2022-11-15 v2.11
  * Fixed adverbially used nominals from advmod to obl.
  * Fixed adverbially used verbs from advmod to advcl.
  * Fixed interjections from advmod to discourse.
  * Fixed non-projective punctuation using Udapi ud.FixPunct.
  * Fixed UPOS tags of copulae: from VERB to AUX.
  * Degree=Sup has been renamed to Degree=Abs in the Latin treebanks.
* 2018-04-15 v2.2
  * Repository renamed from UD_Latin to UD_Latin-Perseus.
  * Numerical suffixes of senses removed from lemmas and stored as LId attributes in the MISC column.
* Since UD v1.2 new texts have been added. More information on the changes in the official github repository (see link above).



<pre>
=== Machine-readable metadata (DO NOT REMOVE!) ================================
Data available since: UD v1.2
License: CC BY-NC-SA 2.5
Includes text: yes
Genre: fiction nonfiction bible
Lemmas: converted from manual
UPOS: converted from manual
XPOS: manual native
Features: converted from manual
Relations: converted from manual
Contributors: Celano, Giuseppe G. A.; Zeman, Daniel; Gamba, Federica
Contributing: elsewhere
Contact: gamba@ufal.mff.cuni.cz
===============================================================================
</pre>
