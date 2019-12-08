# StackOverflow-Tag-Prediction
We have to predict the tags from the tile and description associated to the questions so that we can better create an ecosystem to send the questions to the right set of people to answer it.<br/>

It is a multi-label classification problem

### Data Description

Source - https://www.kaggle.com/c/facebook-recruiting-iii-keyword-extraction/data

### Attribute Information

Field Name | Description
---------- | -----------
Id | Unique idenfier for each question
Title | Tile of the question as the name suggest
Body | description of the question 
Tags | Tags assigned by the person who posted that question

### Analysis
  - Frequency of the tags
  
![](https://github.com/rohitgurjar058/StackOverflow-Tag-Prediction/blob/master/Images/frequency_tags.png)

  - Predict what's the most frequent number of tags found in most of the questions
![](https://github.com/rohitgurjar058/StackOverflow-Tag-Prediction/blob/master/Images/number_of_tags_each_question.png)

  - WordCloud to represent which tag is more frequent
  
  ![](https://github.com/rohitgurjar058/StackOverflow-Tag-Prediction/blob/master/Images/wordcloud.png)

### Model Comparision

Model  | Featurization  | Loss |  Micro F1 Score
------ | -------------- | ---- | --------------
OneVsRest+SGD Classifier  | Tf-idf | log | 0.3738
OneVsRest+Log Reg. Classifier  | Tf-idf | log |  0.395
OneVsRest+SGD Classifier  | Bag-of-words |  log | 0.292
OneVsRest+SGD Classifier  | Bag-of-words |  Hinge | 0.3026

### References

Applied AI Course
