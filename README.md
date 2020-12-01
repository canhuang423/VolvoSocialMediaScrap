# VolvoSocialMediaScrap – Volvo Social Media Crawler & Predictor #2 (DATA-X)
#### *A repository for web scraping of  Volvo car reviews* 

#### By: Sixu Meng, Zhecan Huang, Xiyu He, Kai Lun Chen, Shreyas Hariharan, Suyash Jaju

## Introduction
We are 6 students from UC Berkeley's Applied Data Science and Venture Applicants course (DATA-X: https://datax.berkeley.edu/). Our group name is VolvoSocialMediaScrap – Volvo Social Media Crawler & Predictor #2. We want to help Volvo enhance their customer service by leverageing data insights from car review websites and help develop future business solutions.

As we have now entered the era of data and information, traditional businesses have begun riding the wave of increasingly powerful data science tools to support their decision making and gather insight for strategic planning. Volvo, a global luxury automotive manufacturer from Sweden that produces more than 700,000 cars per year, is similarly looking to assemble all the raw data from the internet and leverage it to improve their business strategy and planning. Most customers and vehicle owners prefer using social media and forums to post reviews and comments about their newly purchased car rather than responding to surveys; thus, it is highly beneficial for Volvo’s business operation team to parse this raw data and extract meaningful information. Hence, this year, Volvo joined forces with 6 UC Berkeley students to build a comprehensive dashboard showcasing essential information extracted from car review websites, notably what customers like or dislike about their Volvos. 

## Web-Scraping 
We scraped Volvo'cars review for 16 types of car models from Edmound, and collected information for their: Vehicle_model', 'Vehicle_Year', 'Vehicle_Rating', 'Review_Date', 'Author_Name', 'Vehicle_Name', 'Helpful_weight', 'Review_Title', 'Customer_Rating', 'Review'. We have a total of 1076 peices of review with above information. 

#### Dataset Collected:
| Volvo Model Name | Reviews (counts) |
| --- | ----------- |
|XC60|244|
|S60|232|
|XC90|223|
|XC40|89|
|XC70|54|
|S90|53|
|V60|46|
|C70|33|
|C30|33|
|V60 Cross Country|26|
|S80|18|
|V90 Cross Country|11|
|V90|10|
|V50|4|
|S60 Cross Country|2|
|S40|1|
|Total|1079|

## Topic Analysis with LDA and NMF

### NMF models
Non-Negative Matrix Factorization (NMF) is a matrix decomposition method, which decomposes a matrix into the product of W and H of non-negative elements. The default method optimizes the distance between the original matrix and WH, i.e., the Frobenius norm. Below is an example where we use NMF to produce 3 topics and we showed 3 bigrams/trigrams in each topic.

### LDA models
Latent Dirichlet Allocation is a generative probabilistic model for collections of discrete dataset such as text corpora. It is also a topic model that is used for discovering abstract topics from a collection of documents.

Here in our example, we use the function LatentDirichletAllocation, which “implements the online variational Bayes algorithm and supports both online and batch update methods”. Here we show an example where the learning method is set to the default value “online”.

## Classifier for positive and negative reviews
Learning from our Data-x's NLP homework, we made a classifier model that can predict good or bad reviews trained by our collected data. We first did some data cleaning such as removing HTML tags, extracting emoticons and non-letter, and appling either stemming or lemmatization. We trained a random forest and a Word2Vec model. Also, we updated our model's vovabulary by adding all the other car's reviews from Edmound website to train our NLP model. The training accuracy is:  1.0, and the validation accuracy is:  0.9568965517241379


## Other Resources:

##### Visualizations: *[Click Here](https://smeng3.github.io/VolvoSocialMediaScrap/).*

##### Story of Project: *[Click Here](https://drive.google.com/file/d/1jNIdr0YYvRiAqAeUiLbnZIr0yQxRonUG/view?usp=sharing)*

##### News Release of Project: *[Click Here](https://docs.google.com/document/d/1__y8xFW6x_ceoO0J9vSxzERt0ygRiZAzwPgxR2AduFo/edit?usp=sharing)*



#### Table of Contents: 
| File Name | Description |
| --- | ----------- |
| LDA.ipynb | Build a model that do topic analysis for reviews |
| NLP Viz.ipynb | LDA and NMF models| 
| NLP.ipynb | | 
| README.md | | 
| Web Scraping.ipynb | Scrap reviews related to Volvo's car from Edmunds| 
| app.py | | 
| app_copy.py | | 
| backup old lda.ipynb | | 
| geckodriver.log | | 
| ldavis_prepared_5 | | 
| ldavis_prepared_5.html | | 
| modeling.ipynb | Build a NLP model that classify pos or neg review using data we scraped|
| old.py | | 
| plot.ipynb | | 




