# KG accountability
The objective of this work is to measure the accountability of RDF graphs. To do so, we define accountability requirements as SPARQL queries. Then, we evaluate many Knowledge Graphs (KG) by querying public SPARQL endpoints using the [IndeGx framework](https://github.com/Wimmics/dekalog). To use IndeGx, we provide a new set of rules dedicated to accountability.
This work is part of the [DeKalog project](https://dekalog.univ-nantes.fr).

## Experiments
This code is made to be used along with [IndeGx](https://github.com/Wimmics/dekalog), version v2.6.2(!) was used for these experiments.
The catalog of SPARQL endpoints used for our experiments is [catalogs/](catalogs/). It is taken from IndeGx.

To evaluate KGs, we proceed in several steps.
1. First, triples corresponding to the metadata of the evaluated KG are extracted using queries in folder [nonTrivialExtractionRules/](nonTrivialExtractionRules/)
2. Then, this extracted triples are saturated by adding equivalent classes and properties, as defined in [equivalencesRules/](equivalencesRules/)
3. The KG is evaluated according to this saturated metadata: [rules/](rules/)
4. Finally, queries in [score_computing_rules/](score_computing_rules/) enable to compute the score of a questions made of a the successions of queries.

A summary of the results is available here: [results/](results/)

## To cite this work
- J. Andersen, S. Cazalens, P. Lamarre, Assessing Knowledge Graphs Accountability. ESWC 2023, Poster and demonstration. https://2023.eswc-conferences.org/wp-content/uploads/2023/05/paper_Andersen_2023_Assessing.pdf

*This work relies on a previous experiment. All catalogs, rules and results of this paper are available in this version of the repository: [v1.0](https://github.com/Jendersen/KG_accountability/tree/v1.0)*

## Description of the Hierarchy and Requirements about Accountability

The accountability requirements has been adapted from the [LiQuID metadata model](https://ceur-ws.org/Vol-2716/paper5.pdf), both its hierarchical structure and the questions illustrating each field of this structure. The organized requirements we defined is illustrated in the following Figure. The correspondance between the LiQuID questions and our adaptation in the context of Knowledge Graphs is available [here](docs/README.md). For a summary of the required properties for each question, see [this file](docs/questions_and_properties.md).

[![Accountability requirements](docs/tag_quest_query.png)](docs/tag_question_query.pdf)
