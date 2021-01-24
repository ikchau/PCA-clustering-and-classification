# Project: Poisonous Mushrooms
## Dimensionality Reduction, Clustering, and Classification

_By Isa Chau for W207: Applied Machine Learning, UC Berkeley School of Information Master of Information and Data Science Program (MIDS), Fall 2019._

**This notebook is based on a project I completed for the MIDS program. In summary, we experiment with PCA, data visualization, and clustering in the pursuit of classifying poisonous mushrooms.**


In this project, we'll investigate properties of mushrooms. This classic dataset contains over 8000 observations, where each mushroom is described by a variety of features like color, odor, etc., and the target variable is an indicator for whether the mushroom is poisonous. Since all the observations are categorical, we've binarized the feature space. Look at the feature_names below to see all 126 binary names.

We'll start by running PCA to reduce the dimensionality from 126 down to 2 so that we can easily visualize the data. In general, PCA is very useful for visualization (though sklearn.manifold.tsne is known to produce better visualizations). Recall that PCA is a linear transformation. The 1st projected dimension is the linear combination of all 126 original features that captures as much of the variance in the data as possible. The 2nd projected dimension is the linear combination of all 126 original features that captures as much of the remaining variance as possible. The idea of dense low dimensional representations is crucial to machine learning!

Once we've projected the data to 2 dimensions, we'll experiment with clustering using KMeans and density estimation with Gaussian Mixture Models. Finally, we'll train a classifier by fitting a GMM for the positive class and a GMM for the negative class, and perform inference by comparing the probabilities output by each model.
