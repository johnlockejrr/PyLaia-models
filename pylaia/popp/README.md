# PyLaia POPP

## Datasets

Trained on the [POPP Generic](https://arkindex.teklia.com/browse/71ab470e-75e0-435b-b0e4-8dbd6ef5a4e9?top_level=true&folder=true) corpus.

| split | N lines |
| ----- | ------: |
| train | 3,835   |
| val   |  480    |
| test  |  479    |

## Results

* Lines resized with a fixed height of 128 pixels
* The language model is a 6-gram character model trained on the training set

| Model                          | test CER | test WER |
| :----------------------------- | :------: | :------: |
| Model without LM               |  16.49   |   36.26  |
| Model with LM (`weight = 1.5`) |  16.09   |   34.52  |
