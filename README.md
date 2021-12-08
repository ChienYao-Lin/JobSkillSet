# Skill-Named-Entity-Recognition-for-Job-Ads

This minor project is for increasing the effectiveness of my [previous course project](https://github.com/ChienYaoLin/skill-searching-public.git). In that project, named-entity recognition model was created by Amazon Comprehend, which needs to wait about 5 minutes to get the prediction and costs money. Hence, The goal of this project is to build a name-entity recognition model with spaCy in order to extract skill entity from job descriptions.

## Requirements
- spaCy: The main package in this project
```bash
$ conda install -c conda-forge spacy
```
- en_core_web_sm: Be used to split the raw into sentences and also be the pre-trained model in the training stage
```bash
$ python -m spacy download en_core_web_sm
```
- entitylist.csv: The data set collected skill entities which I scrape [AngelList](https://angel.co/)'s skill report, but the page is not available now. Here is how the page looked like. ![](https://i.imgur.com/K9QCrAU.png)
- **NOTE**: numpy version should be greater than 1.20 to avoid the [bug](https://github.com/conda-forge/numpy-feedstock/issues/229) on MacOS.


## Conclusion and Future Works
Overall, both of the two model have good performance on test data so I might try to implement them into my AWS project. However, the data set is collected for data analyst, data scientist and data engineer, which may cause the model not suitable for other jobs. Hence, for those who want to use the model but for different jobs, please re-run the jupyter notebook for your job titles.

## Reference
- spaCy, Rule-based entity recognition - https://spacy.io/usage/rule-based-matching#entityruler
- crusaderky 2021, numpy 1.20 on MacOSX: spurious RuntimeWarning: invalid value encountered in reciprocal - https://github.com/conda-forge/numpy-feedstock/issues/229