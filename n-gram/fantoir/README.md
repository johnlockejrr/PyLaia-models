# LM models trained on Fantoir api data

## Details

These models were trained for [this issue](https://redmine.teklia.com/issues/6746). The goal was to get data from the Fantoir api relative to a given department and train a LM model with this data and then use the LM in conjunction with an OCR model to predict the addresses in given address zones for a given department in hopes that this will improve the OCR results.
The text files used to evaluate these models could be found [here](https://redmine.teklia.com/issues/6746#note-45).
These models were trained using this [doc](https://atr.pages.teklia.com/pylaia/usage/language_models/) and evaluated using `kenlm`.

## The results

* models filtered by year on filtered text 

| |txt 04 |txt 27 |txt 29 |
|--|--|--|--|
| arpa 04 | 7.3| 9.3| 16.7 |
| arpa 27 | 9.3 | 7.7 | 16.0 |
| arpa 29 | 9.8 | 9.7 | 9.5 |

* models filtered by year on unfiltered text

| |txt 04 |txt 27 |txt 29 |
|--|--|--|--|
| arpa 04 | 8.5 |8.9|  23|
| arpa 27 | 9.4 | 7.3 | 21.5 |
| arpa 29 | 10.1 | 9.1  | 9.7 |
 
* models not filtered by year on filtered text 

| |txt 04 |txt 27 |txt 29 |
|--|--|--|--|
| arpa 04 |8.3 | 9.1 |17.7 |
| arpa 27 | 9.7| 7.9 | 17.9 |
| arpa 29 | 13.0| 12.3 | 11.1|

* models not filtered by year on unfiltered text

| |txt 04 |txt 27 |txt 29 |
|--|--|--|--|
| arpa 04 | 8.0 | 8.6 | 25|
| arpa 27 | 9.6 | 7.3 | 23.4 |
| arpa 29 | 13.1 | 11.8 |7.6|
