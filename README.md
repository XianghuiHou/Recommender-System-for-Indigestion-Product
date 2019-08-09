# RecommenderSystem
## Introduction
Recommender systems are among the most popular applications of data science today. They are used to predict the "rating" or "preference" that a user would give to an item. Almost every major tech company has applied them in some form or the other: Amazon uses it to suggest products to customers, YouTube uses it to decide which video to play next on autoplay, and Facebook uses it to recommend pages to like and people to follow.

Broadly, I built three recommender systems using Amazon Indigestionproduct review dataset(7000 records)

1.Simple recommenders: offer generalized recommendations to every user, based on product popularity. The basic idea behind this system is that products that are more popular and critically acclaimed will have a higher probability of being liked by the average buyers. 

2.Content-based recommenders: suggest similar items based on a particular item. This system uses item metadata, such as category, ingredient, description, review, etc. for product, to make these recommendations. The general idea behind these recommender systems is that if a person liked a particular item, he or she will also like an item that is similar to it.

3.Collaborative filtering engines: these systems try to predict the rating or preference that a user would give an item-based on past ratings and preferences of other users. Collaborative filters do not require item metadata like its content-based counterparts.

## 1. Simple recommenders (based on weighted rating):
The following are the steps involved:

Decide on the metric or score to rate indigestion product on.
Calculate the score for every indigestion product.
Sort the indigestion product based on the score and output the top results.

Weighted Rating (WR) = (v/(v+m)*R)+(m/(v+m)* C)

where,
v is the number of votes for the product;
m is the minimum votes required to be listed in the chart;
R is the average rating of the product; And
C is the mean vote across the whole report

## 2. Content-Based Recommender (based on user review)
In this section, I will try to build a system that recommends products that are similar to a particular product. More specifically, I will compute pairwise similarity scores using " Cosine Similarity "  for all movies based on their reviews and recommend products based on that similarity score. This recommender will return the productIds corresponding to the indices of the top 10 elements.

## 3. Collaborative filtering engines (predict a user’s response to a product)
In order to predict a user’s response to a product, it is necessary to understand the tastes of the user and the properties of the product. The taste of the user can be learned from user’s review of various products. The properties of the product can be obtained by mining the reviews given by multiple users. Attainment of the tastes of the user and properties of the product will allow us to estimate whether a user will have positive or negative reactions to the products. 
In order to do so, the model: <br/>
● Step 1: attempts to find similar products based on qualitative reviews. <br/>
● Step 2, compares quantitative review and qualitative review to create a connection between the two distinctive scales <br/>
● Step 3: analyze each user’s qualitative review and recommend the products using Step 1 and filter out the low ranking  products by incorporating Step 2 With these steps, the model is able to create a strong recommendation for the customers by comparing the quantitative and qualitative review of the sample population with the specific customer’s reviews.

I firstly built KNN (k=17) with model accuracy =83.82%.
Then I built base Random Forest with model accuracy= 83.04%
In addition, I used random grid search to tune hyperparameter in Random Forest and improved model accuracy to 84.98%.


