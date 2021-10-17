# Predict Hotel Rating from reviews
- Steps followed in this notebook
  - Data Cleaning
  - Tokenization
  - Visualization 
  - Word Cloud Generation
  - Classification
 
 ## Observations 
 - Some reviews had 0 rating and some had rating above 5, so I filtered out those reviews.
 - Since the main idea of analysis had to be depended on the review I tokenized them in three categories : 
  - The original unaltered review
  - Limited review filtered to have no stopwords
  - review that only contains the adjectives of the review
 - It was observed that the reviews were only about hotels in the US but the reviews were also in languages other than english, so i visualized the location of the reviews.
 ![newplot](https://user-images.githubusercontent.com/64835443/137616502-29c34db6-bad6-4eaa-a465-f1a68b2cd054.png)
 - Plotting the reviews on the globe 
 
![globe](https://user-images.githubusercontent.com/64835443/137616646-896d2035-54cc-4192-b1b4-1c41d9cafbea.png)

- Generating Word Cloud

![word_cloud](https://user-images.githubusercontent.com/64835443/137616836-ae2e1801-bee5-47a9-9310-e19d2b68c910.png)

- By plotting a graph for review length, we can observe that the reviews are fairly short and appear to have a bit of a bimodal distribution.
- Accuracy check on classifications found that :
  - Original review text seemed to be best at classifying the reviews.
  -  Linear svc and naive bayes are both comfortably better than chance at predicting the rating of the hotel review
- After plotting the confusion matrix it was found that the fact that there are many more 4,5 star ratings than any other rating, which means the classifier is going to be trained to be much better at identifying these high ratings.
 But even with this issue, the classifier was mainly confusing rating that were next to each other (e.g. confusing a 4 for a 5), which is understandable given how free text reviews don't always match perfectly with a star rating. Overall, the results are fairly good for such a small data set and considering that I did not do any feature selection or even much tuning of the classifier itself. 
