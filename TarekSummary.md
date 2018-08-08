The goal of this project was to explore US Census data from 1994 and establish which characteristics or demographics correlated most strongly with the income threshold of $50K.

##Project Design:

I began by exploring the hygiene and status of the dataset. It was decent, but there was missing data (roughly 10% of the dataset) and crossover in terms of features. My first priority was to iron out the inconsistencies in the dataset. I did this by getting rid of missing values (for the time being) and conglomerating overlapping features. Afterwards, I plotted ROC curves of several different out-of-the-box models to determine which models would make most sense to optimize. I also looked at various avenues of feature engineering, primarily RFE, and methods to fill in the gaps, such as clustering via KMeans/TSNE and oversampling via SMOTE.

Following my exploration, I attempted to design my analysis in a modular fashion, such that I could input a model name and output a set of diagnostic plots based on an optimized grid via a pipeline. I used my business use cases to narrow down two models, one optimized for recall, the other for accuracy.


##Other note:

I'd started with Mushroom classification, but pivoted to this project for better modeling opportunity. I used the opportunity to explore clustering, which unfortunately didn't pan out. Had I had more time, I would've done further analysis on messier, more recent US Census data, or built something on Flask. 


##Tools:

For visualization: Bokeh.
I did not use Flask/SQL.


##Data:

US Census data from 1994, obtained from Kaggle.


##Algorithms:

For analysis: the standard algorithms taught in class (LR, SVM, GBC, DT, RF, DummyClassifier, BC, KNN). I also explored Kmeans and TSNE for imputation via clustering, however I determined these wouldn't impact my model significantly, so I ended up dropping the missing values in the end. I also _played_ with Keras and a neural network, but I didn't end up using it in my analysis, or even really know what I was doing.
