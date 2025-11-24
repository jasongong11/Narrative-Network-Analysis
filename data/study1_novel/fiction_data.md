# Data Analysis Pipeline

1. Raw data is collected from the [Standardized Project Gutenberg Corpus](https://github.com/pgcorpus/gutenberg), which was curated from the [Gutenberg Project](https://www.gutenberg.org/).
2. The raw data were minimally preprocessed and filtered through a pre-defined criterion following a past study ([Knight et al., 2024](https://www.science.org/doi/10.1126/sciadv.adl2013#sec-4)).
3. The preprocessed texts are fed into the [booknlp](https://github.com/booknlp/booknlp) pipeline.
4. The events triplets are extracted from booknlp output files, and constructed into networks as [NetworkX](https://networkx.org/en/) objects. We then measured the corresponding network metrics using NetworkX functions.
5. Finally, the statistical analysis is conducted using the [statsmodel](https://www.statsmodels.org/stable/index.html) package. 