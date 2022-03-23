## Meetings

Meeting: 2022-03-22, 15:00

- Introductions (what is your experience with NLP on historic texts? keep it brief)
- Use cases (5-10 minutes each):
  - Ryan Brate - polyvocality in 19th and 20th century Dutch cultural heritage texts
  - Dirk Roorda - line-layout detection, speck-removal prior to OCR in Arabic text
  - Marijn Koolen - word embeddings in 18th century resolutions

- Open discussion, sharing resources, ...
- When to meet again? Should this be a regular meeting?

### Notes

Questions:

- Dealing with OCR vs. HTR: is there any meaningful difference in the issues we have to deal with?
- How can we get a sense of the size of the problem?
    - how is the sensitivity of the information extraction task related to the amount of historical linguistic variance and text recognition errors?
- Do different languages have different challenges in terms of information extraction from digitised text

Ryan's presentation:
- matching partial trees: look at Corpus Query Language (CQL) and databases like BlackLab, MTAS, SketchEngine
- dependency parse of Alpino is better than that of Frog, but Frog is more robust against very long sentences and messy sentences (and faster)
- CLARIAH tools: [GrETEL](https://gretel.hum.uu.nl/ng/home)
- DR: graph template searching in Text-Fabric: https://annotation.github.io/text-fabric/tf/about/searchusage.html
- DR: see [trgrep2](https://web.stanford.edu/dept/linguistics/corpora/cas-tut-tgrep.html)

Dirk's presentation:
- look at edit diff instead of edit distance
    - See the notebooks on [wp6-daghregisters](https://nbviewer.org/github/CLARIAH/wp6-daghregisters/blob/master/programs/diffanalysis.ipynb)
    - Analiticcl also uses these diff patterns to penalise patterns that are/are not OCR mistakes
- Pre-OCR clean-up: speck removal, deskewing, dewarping
    - need some feedback from linguistic knowledge to avoid removing specks that are part of characters.
    - This is a more general issue with interaction between OCR pipelines and text analysis pipelines (e.g. DI Team's Images and Text)

Marijn's presentation:
- Can we measure the size of the spelling variation problem? 
- TO DO: upload notebook

