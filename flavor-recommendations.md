# **Unsupervised/NLP Project Write-up**
## **Ice Cream Flavor Market Research and Recommendation**
#### *by William Grennan*


## Abstract
The goal of this project was to aggregate and quantify ice cream reviews for the largest four ice cream manufacturers. Using the results of the market research, recommendations for flavors are assigned. These recommendations are based on how others are likely to describe the flavor; it could be sweet, smooth, chunky, or rich. The recommendation will be a flavor similar to that description.


## Design
This project model is built from the 10 mos commonly used adjectives in the list of reviews for each flavor, with positive reviews (5 stars) and negative reviews (1 or 2 stars) split up. These adjectives and flavors are turned into a sparse matrix. Flavor recommendations are created through cosine similarity, with the top 5 flavors being the recommendations - excluding the origin flavor.


## Data
Data for the project was obtained from Kaggle. The data includes 241 flavors from Ben and Jerry’s, Häagen-Dazs, Breyers, and Talenti. All flavors contain an overall score out of 5 stars. The primary data used is the review set which contains 21,674 reviews in pure text format which link back to a specific flavor.

[Kaggle Ice Cream Data](https://www.kaggle.com/datasets/tysonpo/ice-cream-dataset)


## Algorithms
#### Data cleaning
Data arrived very clean, however spaCy was used to process the text and label the adjectives.

#### Models
After the data model is built, the recommendations are created using cosine similarity. The top 5 flavors that match the adjectives used are the flavors most similar to the origin flavor. Adjectives were chosen because of the otherwise high similarity between reviews.


## Tools
- spaCy is used to process the text reviews and to do part of speech labeling
- Pandas and numpy are used for data preperation


## Communications
This work along with the slides and python script has been uploaded to my Github
