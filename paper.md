# Machine Learning – Dimension Reduction (PCA & t-SNE)


## Introduction
When we get a expression matrix RNA-seq, in which every row is a gene, and every column is a sample, how should we get a general sense of the distribution of the data in and how can we extract important features (genes) from the data matrix? Note that the expression matrix is in a high dimensional space because every gene is a dimension. So directly visualizing the data is impossible for human beings. Dimensionality reduction techniques such as PCA and t-SNE can map the original data in high dimensional space to lower dimension while retaining some spatial information. In this way, we can easily visualize the data in 2D space. In addition, PCA can return the “importances” of the features (genes), which are the ability of these features in grouping and separating the data points. By extracting the most important genes from the raw data matrix, we are able to explore the data such as performing clustering more easily. 
  
![]()

## PCA

## T-SNE

## Comparison

PCA has the advantages of definite results and fast run time. It is often used in the earlier stage data analysis step to extract important features (genes) for downstream analysis. And since the resulting principle components are linear combinations of original data, the results can be relatively well interpreted. However, as a data visualization method, it often suffers from the “crowding problem”,in which the somewhat similar points in the high dimensional space collapses in 2D space. For data with many outliers, the non-outliers are force to collapse together and the information for the internal variations among the non-outliers is lost in the process. 

In contrast, t-SNE is computationally expensive and take several hours on million-sample datasets. It is non-deterministic, different run would renter different results, and by providing different perplexity, the resulting clusters would change dramatically. But, as a visualization method, it can relatively show the internal structures of the data well since it preserves the local neighborhood information of the original data in high-dimensional space.

PCA and t-SNE both have advantages and disadvantages. Because of their different focuses, people often apply them in combination for different purposes. PCA is often used to derive the most important features (genes) from the data and make the dataset smaller. And t-SNE is often applied to the filtered dataset for visualization. 

Note that PCA and t-SNE are only two popular dimension reduction methods. There are many more state-of-the-art methods better serving this purpose, such as ICA and UMAP. 


