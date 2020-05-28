# Sentiment text analysis using lexical resources

- Folder util:
    - loader.py - contains functions for loading resources
    - converter.py - contains functions for converting
    - serbian_stemmer.py - https://github.com/nikolamilosevic86/SerbianStemmer
    - wordnet_helper.py - class for manipulating data from wordnet (english and serbian)
    - classifier_helper.py - file for creating model for svm classifier
    - constants.py - contains string constants for rating documents
- Folder tests:
    - contains tests for functions in project
- main.py - main file
- Pdf document - LaTeX project: https://www.overleaf.com/read/syksdbwjhndc

    
## Input data:
- Download all input data and locate them in folder src/input_data:
    - Serbian corpus (3 classes) - film reviews: https://github.com/vukbatanovic/SerbMR (SerbMR-3C - csv format),
        - positive (841), negative (841) and neutral (841) reviews
    - Serbian corpus (2 classes) - film reviews: https://github.com/vukbatanovic/SerbMR (SerbMR-2C - csv format),
        - positive (841) and negative (841) reviews
    - English corpus - film reviews: http://www.cs.cornell.edu/people/pabo/movie-review-data/review_polarity.tar.gz
        - positive (1000) and negative (1000) reviews
    
## Libraries:
- re
- pathlib
- csv
- os
- chardet
- nltk
- transliterate
- pandas
- xml
- string
- sklearn
- numpy

## Results:
- Unsupervised:
    - English corpus (2 classes):
        - precision: 56.79%, recall: 85.7%, f measure: 68.31%, accuracy: 60.25%
    - Serbian corpus (2 classes):
        - precision: 53.56%, recall: 82.28%, f measure: 64.88%, accuracy: 55.47%
    - Serbian corpus (3 classes):
        - precision: 62.14%, recall: 95.25% f measure: 75.22%, accuracy: 62.61%
        - 0.02 precision: 55.26%, recall: 88.59%, f measure: 68.06%, accuracy: 56.63%

- Supervised:
    - English corpus (2 classes):
        - negative: precision: 77%, recall: 80%, f measure: 79%
        - positive: precision: 78%, recall: 74%, f measure: 76%
    - Serbian corpus (2 classes):
        - negative: precision: 71%, recall: 68%, f measure: 70%
        - positive: precision: 68%, recall: 71%, f measure: 69%
    - Serbian corpus (3 classes):
        - negative: precision: 49%, recall: 49%, f measure: 49%
        - neutral: precision: 45%, recall: 50%, f measure: 47%
        - positive: precision: 53%, recall: 47%, f measure: 50%
## References:
- Manning, Christopher D., and Hinrich Schütze. Foundations of statistical natural language processing.
Vol. 999. Cambridge: MIT press, 1999.
- Bird, S., Klein, E., & Loper, E. Natural language processing with Python: analyzing text with
the natural language toolkit. " O'Reilly Media, Inc.". 2009. (http://www.nltk.org/book/)
- Denecke, Kerstin. Using SentiWordnet for multilingual sentiment analysis. Data Engineering
Workshop, 2008. ICDEW 2008. IEEE 24th International Conference on. IEEE, 2008.
