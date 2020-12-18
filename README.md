## Assessing modern classification models and resampling techniques for imbalanced data
### Abstract
The paper compares Logistic Regression and Random Forest in the task of classifying imbalanced data. Other models are known to perform well for this type of problem. We will explore these techniques to improve the predictions on the Civil War Dataset. We will train a Multilayer Perceptron and a Boosting model to assess how well they perform compared to paper’s classifiers. Moreover we will assess how all these models perform with a data augmentation seeking to reduce class imbalance.  

We will then introduce a new dataset about urban social unrest to our analysis. We hypothesize that risk factors for social unrest are similar to those for civil wars, so the classifiers we developed should have decent predictive power on these events.  We consider this question to be important because social unrest in modern contexts, particularly developed nations, can be understood as a sort of pseudo-civil war without state failure.

### Research Questions
- Do state-of-the-art classifiers (MLP and boosted methods) outperform the more classical classifiers (RF, logistic regression)?
- Can resampling and data augmentation methods improve the predictions ?
- Are these approaches successful at predicting urban social unrest / protest events as well?

### Proposed dataset

- https://drive.google.com/drive/folders/1d65RZMdhfFpCLFSlPDPsa7gKDnMdMJ5m Our initial dataset, the Civil War Data (CWD)
- https://www.prio.org/Data/Armed-Conflict/Urban-Social-Disorder/ : Peace Research Institute Oslo’s Urban Social Disorder dataset.This dataset compiles urban social disorder events occuring in capitals and other major cities of the developing world through the 1960-2014 period. We will produce a general indicator from these events that characterizes the level of tension in a given country’s urban areas and assess how the models trained on the CWD are able to predict this indicator.

### Methods
- **New models**: We will use new classifiers (Boosted tree classifier and Multilayer Perceptron) and use them on the CWD, in a similar fashion to the original paper’s first part.
- **Direct handling of class imbalance**: We aim to tackle class imbalance by using data augmentation / resampling, namely we plan on using the SMOTE algorithm.
- **Urban Social Disorder (USD) Dataset**: From the USD, we will use the two features `BYEAR` and `GWNO` to merge it with the CWD. We will use the feature `PTYPE` (Problem Type) to develop a simple measure of urban unrest. We will then merge this urban unrest factor with the CWD and use CWD's features will all the classifiers we developped so far to see if these can predict urban disorder effectively. 

### Proposed timeline

- **Week from 30/11 - 06/12**: Implementing the two news models, evaluating performance through metrics and visualizations. Comparing them with the paper’s original results. Investigating reasons for success / failure. Implement the SMOTE algorithm and use it on the CWD.

- **Week from 07/11 - 13/12**: Evaluate the performance benefits gained by using the SMOTE algorithm to balance the data through metrics and visualizations. Processing PRIO data, and develop a method to regroup events into a relevant social unrest metric(s) country-wise and year-wise (just like in CWD).

- **Week from 14/12 - 18/12** : Write the report. Prepare the video. Evaluate the performance of the predictive models on the PRIO data through metrics and visualizations.

### Organization within the team


- For week 1 Maxime will use boosted trees to evaluate their performance. He will make some visualizations similar to the one in the paper to make a comparison. Alex will be doing the same with the MLP. Arnaud will work on the implementation of the SMOTE algorithm and use it on CWD.

- For week 2 Arnaud will evaluate the results of the SMOTE augmentation on previous techniques. Group will discuss how to craft interesting features from the PRIO dataset and try some implementations.

- For week 3 Maxime will work on the report, Arnaud and Alex will prepare the video.


- Maxime: implemented boosted trees, worked on visualizations and model comparaison analysis, integrated USD dataset


### Tasks done

- Maxime: Evaluated performance of boosted trees, worked on data visualizations and model comparaison analysis for report, integrated USD dataset, report writing
- Arnaud: added SMOTE resampling and associated F1 testing and visualizations, helped integrate USD data, report writing
- Alexander: Evaluated performance of Multilayer Perceptron, data scaling, conducted data exploration and report review.