# CMPE255_Dimensionality_Reduction

## Various Dimensionality Reduction Techniques
_i) PCA
ii) SVD
iii) LLE
iv) t-SNE
v) ISOMAP
vi) UMAP_

## Tabular Data:

**Info About Dataset:**
The ANSUR II working databases contain 93 anthropometric measurements which were directly measured, and 15 demographic/administrative variables explained below. The
ANSUR II Male working database contains a total sample of 4,082 subjects. The ANSUR II Female working database contains a total sample of 1,986 subjects.

**NOTE:** I did not feature extract the dataset; instead, I used all of the features solely for visualization.

**Linear Dimensionality Techniques:**
The plots of PCA and SVD in the dataset are quite similar, which makes sense because the basic decomposition mechanism is similar in both methods.

**Non-Linear Dimensionality Reduction Techniques:**
In 2D/3D, UMAP/t-SNE offered higher clustering results ( example: check gender clustering). It was particularly useful for showing clusters or groups of data points, as well as their relative distances. The main distinction between UMAP and TSNE is its scalability; it can be applied directly to sparse matrices, obviating the necessity for dimensionality reduction techniques like PCA or SVD. In the dataset, UMAP is also more faster than t-SNE and preserves more of the global structure.

Our dataset's clustering was likewise well-served by ISOMAP embedding. LLE uses KNN in a similar way to ISOMAP, but the visualization was considerably different from the other techniques. In addition, LLE computations are faster than ISOMAP computations.

## Image Data:

**Dimensionality Techniques on the Fashion Dataset:**

**Info about Dataset:**
Zalando research published a new dataset, which is very similar to the well known MNIST database of handwritten digits. However, instead of having images of the digits 0–9, Zalando’s data contains (not unsurprisingly) images with 10 different fashion products. The dataset is called Fashion-MNIST dataset.

The 10 different class labels are:
_0: T-shirt/top,
1: Trouser,
2: Pullover,
3: Dress,
4: Coat,
5: Sandal,
6: Shirt,
7: Sneaker,
8: Bag,
9: Ankle boot_

**Linear Dimensionality Techniques:**
If we want to compress images into lesser dimensions while preserving the info for image classification task, we can use PCA/SVD. It's feasible to do it with just 80 components while still maintaining about 90% of the image.

PCA/SVD fails to cluster the fashion category data points based on the actual information they carry with 2/3 components in projections. 

**Non-Linear Dimensionality Reduction Techniques:**
Even with a small sample of 1000 observations, all Manifold learning approaches did a far better job of creating beautiful clusters.
t-SNE generates good clusters of various fashion items, each of which is visualized as a block. UMAP was substantially faster, implying that it can handle massive datasets and data with many dimensions. Despite the peaks, LLE was capable of capturing better cluster structure.
