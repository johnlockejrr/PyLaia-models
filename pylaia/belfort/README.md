# PyLaia Belfort

## Datasets

This model is trained from scratch on the [Belfort](https://demo.arkindex.org/browse/d6fe867e-d3dc-4a40-b5e8-c54b08f79137) corpus:
* PyLaia is trained on ROVER annotations created from [Callico](https://callico.teklia.com/projects/ce9b42d4-23a8-4381-b5bb-459bedc59165/details/), [DAN](https://demo.arkindex.org/process/worker-version/d40bdd30-1913-469c-a0ff-4f49558e59b6), [PyLaia](https://demo.arkindex.org/process/worker-version/155854f5-21e3-4d60-9d81-d6d2cbd9ddee) transcriptions
* The ARPA language model is trained on Callico annotations

The following (random) splits are used:
* [train set](https://demo.arkindex.org/element/3cd76b7a-af1a-436b-8d81-e9fa6d62323b),
* [validation set](https://demo.arkindex.org/element/ddd9979f-3fdb-4dbc-bdb1-1e0dc9577a3b),
* [test set](https://demo.arkindex.org/element/93f02102-23bc-477d-8b96-701ce92487d0).

The dataset is available in `/home/training_data/ATR_line/Belfort/belfort_final/`.

## Results

* Support: 19751 (train) / 2770 (validation) / 2490 (test)
* Best LM weight: 2.0
* Redmine issue [#2531](https://redmine.teklia.com/issues/2531)

| Model           | val CER | val WER | test CER | test WER |
| --------------- | ------- | ------- | -------- | -------- |
| PyLaia          | 8.78    | 23.54   | 7.96     | 23.25    |
| PyLaia + 6-gram | 8.06    | 19.63   | 7.34     | 19.78    |

