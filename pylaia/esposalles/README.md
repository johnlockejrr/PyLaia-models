# PyLaia Esposalles

## Datasets

Trained on text-lines from the [Esposalles](https://arkindex.teklia.com/browse/42ab0534-1816-4b11-a0e9-02c543f9e9b3?top_level=true&folder=true) corpus.

| split | N lines |
| ----- | ------: |
| train | 2,328   |
| val   |   742   |
| test  |   757   |

## Results

* Lines resized with a fixed height of 128 pixels
* The language model is a 6-gram character model trained on the training set

| Model                               | test CER | test WER |
| :---------------------------------- | :------: | :------: |
| Model without LM                    |  0.76    |   2.62   |
| Model with LM (`best weight = 4.0`) |  1.04    |   3.38   |
