
# Exploratory data analysis for finding explicit links between Norwegian news articles 

To this end, we aim to investigate:
-	How can a high-performance NLP – based model be developed for finding similar content from a massive amount of unlabeled data?
-	Which publishers often share stories or publish similar articles? 
-	Which are the most discussed personalities in Norwegian publishments extracted using Named Entity Recognition?
-	 Nouns describe the main features of a story - Who, What, Where. Can restricting our analysis to nouns improve similar story detection?
-	Results and evaluation of the implemented model




## Table of Contents
### Primary purpose - Finding similar articles and trends among publisher
- Exploratory data analysis
- Extracting Nouns
- Observing similar articles manually
- Preprocessing of seelcted features from the data
- Applying similarity matrix and agglomerative clustering to first 1000 articles
- Applying agglomerative clustering to complete dataset
- Evaluation
- Visualization
### Secondary purpose - Named entity recognition
- Named entity recognition
- Extracting personalities from the title of news articles

## Exploratory data analysis
The data set is owned by a private company, to evaluate what the dataset contains we performed a detailed investigation on the dataset in the file .
- Web64_EDA - Final .ipynb
We have selected feature title from the dataset to find similar norwegian articles
## Extracting Nouns
For a laptop, perdorming analysis on more than one lac textual datapoint can be burdonsome, thus we have extracted the nouns of the tiles of the articles to lower the load on machines.
We have use the toolkit provided by SpaCY. The file mentioned below has the the implementation of extracting nouns

- Web64_extracting nouns from the dataset.ipynb

## Manually observing similar articles
We have just go through the dataset manuallay to find some examples of simialr articles published by Norwegian news. The file mentioned below has the details.
- web64_manually observing similar articles in the dataset.ipynb
## Data preprocessing 
The data set has details of Norwegian articles. We have implemented NlP techniques to deal with Norwegian text
- Stop word removal
- Snowball stemming
- Tokenization
- TF-IDF
The file mentioned below has the implementaion
- Web64_initial step of grouping similar articles .ipynb
## Cosine simialrity and agglomarative clustring
We have used cosine similarity to identify how TF-IDF is working
and then applied agglomerative clustering with complete linkage and euclidean as affinity to make clusters of similar articles. We have used PCA to identify n_clusters.
File mentioned below has the impolementation
- Web64_initial step of grouping similar articles .ipynb
## Full dataset
We have applied cosine similarity to full dataset and made clusters of similar articles
The implementation is in file mentioned below
- Web64_ agglomerative clustering on full dataset.ipynb
## Evaluation
We have used nouns of the titles to group simialr articles, their is a previously implemented model using same techniques by Marina Fredmin.
Thus, we have evaluated our model with hers using fowlkes mellow score
We also use silhoutte score to evaluate the coherence of our clusters
The file mentioned below has the implementation
- Web64_evaluation.ipynb
## Visualization
We have analyzed trends of publishers which uploads unique or simialar stories, we gave labels to each articles whether it is unique or similar to another publication.
The file mentioned below has the implementation.
- Web64_final visualization of domains.ipynb 
## Named entity recognition
As a secondary task of the thesis we have analyzed named entity recognitions from the titles of the articles
we have used SpaCy to extract entities
The file mentioned below has the implementation
- Web64_named entity recognition_final.ipynb
## Personalities
We have noticed that personalities mentioned in the titles donot hold ful names, thus we have changed the single names to the full names
We have analyzed trends about what are the top discussed personalities in Norwegain news from November 1 to November 7
The file mentioned below has the implementatoion
- Web64_personalities _final.ipynb