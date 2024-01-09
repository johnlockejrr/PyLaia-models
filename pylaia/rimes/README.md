# PyLaia Rimes

## Datasets

Trained on text-lines from the [Rimes 2011 dataset](https://teklia.com/research/rimes-database/).

| split  | N lines |
|--------|--------:|
| train  | 10,188  |
| val    |  1,138  |
| test   |    778  |

## Results

* Fixed line height: 128 pixels
* Language model: 6-gram character model trained on the training set with KenLM

| Model             			  | val CER | test CER | val WER | test WER |
|:--------------------------------|--------:|---------:|--------:|---------:|
| Model without LM 	              | 4.55  	| 4.53 	   | 14.39   | 15.06    |
| Model with LM (`weight = 1.5`)  | 3.68    | 3.47 	   | 10.01 	 | 10.20    |
