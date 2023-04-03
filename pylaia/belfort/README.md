# PyLaia Belfort

## Datasets

This model is trained from scratch on the [Belfort](https://demo.arkindex.org/browse/d6fe867e-d3dc-4a40-b5e8-c54b08f79137) corpus.

Transcriptions were created in [Callico](https://callico.teklia.com/projects/ce9b42d4-23a8-4381-b5bb-459bedc59165/details/). Some lines were annotated by two different annotators, others by a single annotator. The following splits are used:
* [train set](https://demo.arkindex.org/element/0609b3a8-c73b-4f6c-a2e3-0125c48a5ac4),
* [validation set](https://demo.arkindex.org/element/abba68d5-9516-469e-8912-4e74ccd669c5),
* [test set](https://demo.arkindex.org/element/43674622-7095-4dcc-a5c6-6587cff75c03).

The distribution strategy of the data in the different splits is detailed below:
* lines with a single annotation are in the train set,
* lines with double annotations and bad agreement (CER > 5%) are discarded,
* lines with double annotations and good agreement (0% < CER < 5%) are randomly split into validation and test sets.

Note: lines with double annotations and perfect agreement are currently in the train set due to an export issue from Callico to Arkindex.

The dataset is available in `/home/training_data/ATR_line/Belfort/belfort_v1/`.

## Results

* Support: 19321 (train) / 499 (validation) / 490 (test)
* Best LM weight: 1.0
* Redmine issue [#3620](https://redmine.teklia.com/issues/3620)

| Model           | val CER | val WER | test CER | test WER |
| --------------- | ------- | ------- | -------- | -------- |
| PyLaia          | 6.29    | 23.61   | 5.43     | 20.64    |
| PyLaia + 6-gram | 5.47    | 20.48   | 4.56     | 17.05    |

