# NLP Resources for dealing with historical texts

[NLP-for-Historical-Text](https://github.com/HuygensING/NLP-for-Historical-Text) repository

## Issues with historical documents

- OCR/HTR errors
- Layout and segmentation
- Spelling variation, especially with text from before 1800 (problem increases with older documents)
- Spelling and vocabulary change (old words disappear, new words appear, existing words shift meaning)


These issues affect search, string matching, syntactical parsing, and the term frequency distribution and context that is used in e.g. embeddings.


## Existing Technologies and Tools

### Pre OCR cleaning/layout-detection/imageprocessing

- OpenCV, NumPy, SciPy
- All together in the [Fusus project](https://github.com/among/fusus) (with Cornelis van Lit, Univ. Utrecht)
- Overview of tech used: [tech](https://among.github.io/fusus/fusus/about/tech.html)

### OCR post correction

- Analiticcl by Maarten van Gompel: 
    - Code: https://github.com/proycon/analiticcl
    - Presentation video: https://diode.zone/w/kkrqA4MocGwxyC3s68Zsq7
    - Presentation slides: https://github.com/proycon/analiticcl/blob/master/docs/pres_20220120/analiticcl_presentation.pdf
- Edit diff rather than edit dist (immature idea Dirk)
    - see [wp6-daghregisters](https://nbviewer.org/github/CLARIAH/wp6-daghregisters/blob/master/programs/diffanalysis.ipynb)
    - see also [sesdiff](https://github.com/proycon/sesdiff)
- [PICCL](https://github.com/LanguageMachines/PICCL) and underlying [TICCLtools](https://github.com/languagemachines/ticcltools), Martin Reynaert, Ko van der Sloot 

### Fuzzy Search and String Matching

- Python libraries for fuzzy search and matching
    - fuzzywuzzy
    - fuzzysearch
    - Fuzzy-search
    - python-levenshtein
    - Python regex module [URL](https://pypi.org/project/regex/)
    - [python-string-similarity](https://github.com/luozhouyang/python-string-similarity)
- Indexing and Search
    - Elasticsearch
        - edit distance search
    - Postgresql
        - edit distance search
    - Recommended blog article: [Index 1,600,000,000 Keys with Automata and Rust](https://blog.burntsushi.net/transducers/)


### PoS, Lemmatisation and NER on historical dutch

* [Nederlab Pipeline](https://github.com/proycon/nederlab-pipeline)
   * uses [Frog](https://languagemachines.github.io/frog) for PoS-tagging and lemmatisation Middle Dutch, and Early New Dutch (vroegnieuwnederlands). Contains models trained on Brieven als Buit corpus (early new dutch) and Corpys Gysseling and Corpus Reenen Mulder (middle dutch).
   * ``FoLiA-wordtranslate`` (part of [FoLiA-utils](https://github.com/LanguageMachines)) - (Re)implements Erik Tjong Kim Sang's word-by-word modernisation method.

### Parse tree querying and extraction

- [GrETEL](https://gretel.hum.uu.nl/ng/home): partial tree extraction
- [BlackLab](http://inl.github.io/BlackLab/): open source corpus search engine that supports Corpus Query Language


## Literature

- Ehrmann, M., Hamdi, A., Pontes, E. L., Romanello, M., & Doucet, A. (2021). *Named Entity Recognition and Classification on Historical Documents: A Survey.* arXiv preprint arXiv:2109.11406.[PDF](https://arxiv.org/pdf/2109.11406)
- Reynaert, M., Hendrickx, I., & Marquilhas, R. (2012). *Historical spelling normalization. A comparison of two statistical methods: TICCL and VARD2.* Proceedings of ACRH-2, 87-98. [PDF](https://www.researchgate.net/profile/Francesco-Mambrini/publication/275348196_Proceedings_of_the_Second_Workshop_on_Annotation_of_Corpora_for_Research_in_the_Humanities_ACRH-2/links/56e1341808aec4b3333d2242/Proceedings-of-the-Second-Workshop-on-Annotation-of-Corpora-for-Research-in-the-Humanities-ACRH-2.pdf#page=95)
- Reynaert, M., Gompel, M. V., Sloot, K., & van den Bosch, A. P. J. (2015). *PICCL: Philosophical Integrator of Computational and Corpus Libraries.* [PDF](https://repository.ubn.ru.nl/bitstream/handle/2066/150918/150918.pdf)
- Sommerauer, P., & Fokkens, A. (2019, August). *Conceptual change and distributional semantic models: An exploratory study on pitfalls and possibilities.* In Proceedings of the 1st International Workshop on Computational Approaches to Historical Language Change (pp. 223-233).[PDF](https://aclanthology.org/W19-4728/)
- Wevers, M., & Koolen, M. (2020). *Digital begriffsgeschichte: Tracing semantic change using word embeddings.* Historical Methods: A Journal of Quantitative and Interdisciplinary History, 53(4), 226-243. [PDF](https://www.tandfonline.com/doi/pdf/10.1080/01615440.2020.1760157)