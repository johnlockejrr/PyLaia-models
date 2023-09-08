# PyLaia Austrian Newspaper (fraktur)

## Datasets

Trained on horizontal text-lines from the [Austrian Newspaper](https://demo.arkindex.org/browse/4dc4af87-20d0-4101-8ce9-6e427517c2b2?top_level=true&folder=true) corpus.

## Results

* Fixed line height of 128 pixels
* LM = kenlm 6-gram character model trained on the training set

| Model      | Split   |   CER (%) |   WER (%) |   Support |
|------------|---------|-----------|-----------|-----------|
| PyLaia     | train   |      1.62 |      5.63 |     38891 |
| PyLaia     | val     |      1.82 |      7.77 |      3282 |
| PyLaia+LM  | val     |      1.77 |      7.01 |      3282 |
