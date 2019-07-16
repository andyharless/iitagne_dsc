This is my solution that tied for first place in the [IITAGNE](https://www.iitagne.org/) Data Science Challenge in Cambridge, MA on 20190316.  The predictions scored r=0.12, which was the highest prediction score, compared to the 2nd highest at around 0.07.

We were presented with a set of (anonymized) tabular data reprsenting characteristics of different stocks and asked to categorize them into 20 bins representing expected future performance.  "Dep_var" is an integoer indicating the bin.

(Looking at the code afterward, I realized there was a bug: I used 3 different models of the same type, but I forgot to reset all the hyperparameters after validation, so the first model was actually the third model, but with fewer boosting rounds.  It turns out that the bug seems to have helped the results slightly: maybe it prevented me overfitting the validation.  See the "post_mortem" file.)

Links to Jupyter files in notebook viewer, in case Github's version flakes:
- [gbm_post_mortem.ipynb](https://nbviewer.jupyter.org/github/andyharless/iitagne_dsc/blob/master/gbm_post_mortem.ipynb)
- [gbm_v6.ipynb](https://nbviewer.jupyter.org/github/andyharless/iitagne_dsc/blob/master/gbm_v6.ipynb)
