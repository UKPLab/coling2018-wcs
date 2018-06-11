# Word Class Suggestion

This repository hosts support code for the paper "From Text to Lexicon: Bridging the Gap between Word Embeddings and Lexical Resources". Please cite the following work:


```
bibtex coming soon
```

> **Abstract:**
Distributional word representations (often referred to as word embeddings) are omnipresent in modern NLP. Early work has focused on building representations for word types, and recent studies show that lemmatization and part of speech (POS) disambiguation of targets in isolation improve the performance of word embeddings on a range of downstream tasks. However, the reasons behind these improvements, the qualitative effects of these operations and the combined performance of lemmatized and POS disambiguated targets are less studied. This work aims to close this gap and puts previous findings into a general perspective. We examine the effect of lemmatization and POS typing on word embedding performance in a novel resource-based evaluation scenario, as well as on standard similarity benchmarks. We show that these two operations have complementary qualitative and vocabulary-level effects and are best used in combination. We find that the improvement is more pronounced for verbs and show how lemmatization and POS typing implicitly target some of the verb-specific issues. We claim that the observed improvement is a result of better conceptual alignment between word embeddings and lexical resources, stressing the need for conceptually plausible modeling of word embedding targets.

Contact person:

Ilia Kuznetsov, kuznetsov@ukp.informatik.tu-darmstadt.de

https://www.ukp.tu-darmstadt.de/

https://www.tu-darmstadt.de/


> This repository contains experimental software and is published for the sole purpose of giving additional background details on the respective publication.

Follow the steps below to reproduce our results. Don't hesitate to contact us if you have further questions or encounter problems.

## Resources

First, get the resources.

1. VerbNet 3.3 (http://verbs.colorado.edu/verb-index/vn/verbnet3.3.zip)
2. WordNet 3.1 (http://wordnetcode.princeton.edu/wn3.1.dict.tar.gz)
3. SimLex-999 (http://www.leviants.com/ira.leviant/SimLex_ALL_Langs_TXT_Format.zip)
4. SimVerb-3500 (http://people.ds.cam.ac.uk/dsg40/paper/simverb/simverb-3500-data.zip)
5. Our embeddings (http://public.ukp.informatik.tu-darmstadt.de/coling2018_wcs/wcs_coling2018_emb.zip)

Unzip everything and put into corresponding folders under `./resources` so that you get the following:

```
resources
..verbnet3.3
..wn3.1
..benchmarks
....SimLex_ALL_Langs_TXT_Format
....SimVerb-3500
..embeddings
....our embedding files
```

## Dependencies

The code has been tested on python 2.7.13. We use some 3rd party libraries, but nothing exotic:

* numpy (1.13.3)
* scipy (1.0.0)
* sklearn (0.18.1)
* pandas (0.20.3)
* gensim (2.2.0)
* seaborn (0.7.1)
* matplotlib (2.0.2)

## Running the experiments

Now run the _WCS.ipynb_ notebook in *jupyter* and follow the steps. The code includes a demo in case you plan to use WCS in an application.
You might need to modify paths in _settings.py_, but that shouldn't be necessary if you follow the suggested folder structure.
