# PyLaia Alcar

## Datasets

* Trained on [HOME Alcar](https://demo.arkindex.org/browse/46b9b1f4-baeb-4342-a501-e2f15472a276?top_level=true&folder=true) and [Himanis](https://arkindex.teklia.com/browse/2f6e26b0-5fdd-4193-bb30-a3162b96280c?top_level=true&folder=true).
* Text-lines are resized to a fixed height of 128 pixels.
* The language model is a 6-gram character model trained only on the training set of HOME-Alcar.

| split | N lines Alcar | N lines Himanis |  Total |
| ----- | ------------: | --------------: | -----: |
| train |        59,969 |          18,504 | 78,473 |
| val   |         7,905 |           2,367 | 10,272 |
| test  |         6,932 |           2,241 |  9,173 |

## Results

* Evaluation on the test set of HOME-Alcar

| Split | LM  | Evaluation method  | CER (%)  | WER (%)   | Support |
| ----- | --- | ------------------ | -------- | --------- | ------- |
| test  | No  | basic              | 8.35     | 26.15     | 6932    |
| test  | No  | escape punctuation | 8.35     | 24.6      | 6932    |
| test  | Yes | basic              | **7.85** | **23.2**  | 6932    |
| test  | Yes | escape punctuation | **7.85** | **21.76** | 6932    |