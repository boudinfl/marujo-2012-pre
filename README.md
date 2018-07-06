# Preprocessed Marujo keyphrase extraction benchmark dataset

This dataset was introduced in:

 - **Supervised Topical Key Phrase Extraction of News Stories using
   Crowdsourcing, Light Filtering and Co-reference Normalization.**
   Marujo, L., Gershman, A., Carbonell, J., Frederking, R., & Neto, J. P.
   *In Proceedings of LREC 2012.*

The dataset is split into four directories:

  * `references`: reference keyphrases for evaluation
  * `test`: test set
  * `train`: training set
  * `src`: scripts and archive from which the dataset is built


Each input file is processed using the Stanford CoreNLP suite v3.6.0.
We use the default parameters and perform tokenization, sentence splitting and
Part-Of-Speech (POS) tagging. Files are in XML format.

Reference keyphrases are in json format and named according to the following
rules:

    [test|train].reader.[stem]?.json

reader-provided (stemmed or not) reference keyphrases for test and train splits.

Stemming (if applied), is performed with nltk Porter algorithm (English).

Below is a toy example of reference file:

    {
        "doc-1": [
            [
                "target detect"
            ],
            [
                "number of sensor",
                "sensor number"
            ]
        ],
        ...
    }
