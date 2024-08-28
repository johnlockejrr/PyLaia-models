# PyLaia CASIA-hwdb2

## Datasets

Trained on text-lines from the [CASIA](https://arkindex.teklia.com/element/824bf9c9-036e-4fa5-9e91-a81578c7acfb) corpus.

| split  | N lines |
|--------|--------:|
| train  | 33425   |
| val    |  8325   |
| test   | 10449   |

## Results

* Line height = 128
* LM = kenlm 6-gram character model trained on the training set
* Note: since there is no space, the WER can be seen as the Line Error Rate.

| Model             		   | test CER 	| test WER 	 |
|:-----------------------------|:----------:|:----------:|
| Model without LM 	           | 4.61 	  	| 50.86      |
| Model with LM (`weight=1.5`) | 1.53 	  	| 24.44      |
