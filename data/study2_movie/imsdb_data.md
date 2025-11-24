# Data Analysis Pipeline

1. Raw HTML data is scraped from [IMSDB](https://imsdb.com/) using the code provided in the code.
2. IMDB metadata is downloaded from the [official non-commercial dataset](https://developer.imdb.com/non-commercial-datasets/).
3. The HTML data is processed by the [imsdb parser](https://github.com/alex-raw/imsdb_parse), which transforms HTML data into XML parsed data, which is annotated by the function of each script line, such as dialog, action, characters, etc.
4. The XML-parsed data is processed by extracting the action lines and fed into the [booknlp](https://github.com/booknlp/booknlp) pipeline.
5. The events triplets are extracted from booknlp output files, and constructed into networks as [NetworkX](https://networkx.org/en/) objects. We then measured the corresponding network metrics using NetworkX functions.
6. Finally, the statistical analysis is conducted using the [statsmodel](https://www.statsmodels.org/stable/index.html) package. 

