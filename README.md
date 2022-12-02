# KG accountability

This work is part of the [DeKalog project](https://dekalog.univ-nantes.fr).
This code is made to be used along with [IndeGx](https://github.com/Wimmics/dekalog).

- It provides a new set of rules to measure accountability of knowledge graphs in [rules/](https://github.com/Jendersen/KG_accountability/tree/main/rules).
- [InformationNeed/](https://github.com/Jendersen/KG_accountability/tree/main/InformationNeed) provides the ontology SIN-O to describe information needs, and a first information need focused on accountability.
- [queries/](https://github.com/Jendersen/KG_accountability/tree/main/queries) contains queries to execute after runnning all rules on a given set of endpoints in order (i) to compute the score for the successions of queries and (ii) to obtain the different scores of accountability on each tag, and the global score.
- [catalogs/](https://github.com/Jendersen/KG_accountability/tree/main/catalogs) was taken from IndeGx. It is the catalog of endpoints used for our experiments.

The queries *q_measure_creator_who.rq*, *q_measure_maintenance_who.rq*, and *q_measure_usage_how.rq* have to be executed first and their results be used for the execution of the other queries.
