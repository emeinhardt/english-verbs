# english-verbs

This repository contains a database of phonologically transcribed English verbs, organized by inflection. This database (`english-verbs-phon.tsv`) is a tab-separated value file where each row contains phonemic transcriptions of 
 - the first person present
 - the third person present
 - the first person past
 - the third person past

The file is produced by reading in data from the CELEX-2 database for English morphological wordforms, and then mapping the orthographic transcriptions of each inflected wordform to transcriptions from the CMU pronouncing dictionary. The CELEX data is not included in this repository; a processed version of the CMU pronouncing dictionary is, however. (Its origin is described in the Jupyter notebook.)

The notebook `Extracting verb inflections from CELEX and aligning them with the CMU pronouncing dictionary.ipynb` documents data processing and origin in detail.

## Requirements for running the notebook and reproducing the data

 - As noted above, you must have (and correctly set the filepath for) a local copy of the CELEX database.
 - The notebook makes use of shell command magics for Unix-like systems (though none of these calls are essential).
 - The notebook makes use of `joblib` for parallelizing data processing. In each case, commented-out code in the same cell that does not require joblib is also present.
