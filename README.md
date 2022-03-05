# SP22_4995_AML_FinalProj
2022 Spring Applied Machine Learning (COMS 4995) Final Project

Daoxing Zhang (dz2479)\
Hyo Won Kim (hk3175)\
Hongzhi Shi(hs3194)\
Ruoxi Liu (rl3155)\
Ziyu Fang(zf2253)

## Data Set Background
This is a data set from kaggel.com ([online-shoppers-intention](https://www.kaggle.com/roshansharma/online-shopper-s-intention)). This data set contains some customers’ behavioral information when visiting online shopping websites and also the results whether they purchased something or not. There are 10 numerical and 8 categorical features in this dataset which has about 1.2k samples. 
## Data Set Description
“Revenue” is what we will make a prediction on, which represents whether revenue will be generated or not based on all other features. In this data set, there are types of pages visited by the users, time and behaviors visitors had during the session. "Bounce Rate", "Exit Rate" and "Page Value" of the shopping website are also included. Time features can be found as well, such as the "Special Day" and “Weekend”. 
Overall, it is a data set with comprehensive information about users and websites. All those characteristics, features and indices are helpful enough to be filtered out as useful tools to analyze users’ behaviors and future tendencies. 
## Questions & Techniques
- Are there any relationships between users’ browsing behaviors and their time spent on the website?
- Which ones have positive or negative impact on the result?
- Can we utilize visitors’ purchase patterns to optimize recommendation systems?
- Do visitors of different types (returning visitors or new visitors) behave differently?
- Which features are important for predicting whether visitors will make a purchase?

The main problem is how to customize the recommended products based on the information about the user, current product and session. To solve those problems mentioned above, we plan to do it in two steps:
The first step is to determine the number of recommended products that are supposed to be shown in the webpage. To do this, we begin with estimating the possibility of purchasing with supervised models like logistic regression and random forest. We would identify and select features that are useful in predicting the purchase possibility. Then we build a simple function to map purchase possibility to the number of recommended products, making sure higher chances of purchasing leads to lower number of recommendations. If a user has a low estimated willingness to purchase, which might lead to a prediction that he might want to exit, we recommend more products to attract the user to stay in the website. On the other hand, if the user is likely to buy, we recommend less to avoid distraction.
The second step is to rank the other products using a recommendation system. We will start with classical models like collaborative filtering, then move on to explore some more advanced techniques like session based KNN. Then we recommend top k products where k is given by the first step.

