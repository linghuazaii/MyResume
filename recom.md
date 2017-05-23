How we do recommendation?
==========================
1. calculate ctr:
    + ctr = (read + 0.7(priority)) / (show + base)
    + why give it a priority and a base? Cause we need to give a base ctr to new articles which has 0 read and 0 show, so they have a chance to be showed in feed. And also, for articles with low read like 1 and low show like 2, make this kind of articles have a lower ctr to make it not always be showed in feed.  

2. calculate lda:
    + a lda model is trained with 300 dimensions
    + all news will calculate a score in this model
    + calculate similarity of user topic and channel article topic 

3. calculate tag score:
    + user tag and article tag
    + calculate tag score

4. GBDT prediction:
    + xgboost gbdt training a model
    + gbdt prediction in algorithm
    + assign gbdt score  

5. 
