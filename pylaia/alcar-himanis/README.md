# PyLaia Alcar & Himanis

## Datasets

* Trained on [HOME Alcar](https://demo.arkindex.org/browse/46b9b1f4-baeb-4342-a501-e2f15472a276?top_level=true&folder=true) and [Himanis](https://arkindex.teklia.com/browse/2f6e26b0-5fdd-4193-bb30-a3162b96280c?top_level=true&folder=true).
* Text-lines are resized to a fixed height of 128 pixels.
* The language model is a 6-gram character model trained only on the training set of Himanis and HOME Alcar.

| split | N lines Alcar | N lines Himanis |  Total |
| ----- | ------------: | --------------: | -----: |
| train |        59,969 |          18,504 | 78,473 |
| val   |         7,905 |           2,367 | 10,272 |
| test  |         6,932 |           2,241 |  9,173 |

## Results

* Evaluation on the test set of Himanis and HOME Alcar (escaped punctuation)

| set   | LM  |       Himanis | support |        Alcar | support |
| ----- | --- | ------------: | ------: | -----------: | ------: |
| train | no  |  5.31 - 17.47 |   18503 | 4.74 - 17.29 |   59969 |
| val   | no  | 10.37 - 27.63 |    2367 | 7.82 - 23.67 |    7905 |
| test  | no  |  9.87 - 28.27 |    2241 | 8.34 - 24.57 |    6932 |
| test  | yes |  8.94 - 23.82 |    2241 | 7.87 - 21.90 |    6932 |
