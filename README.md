# 🧩 Dimensionality Reduction with PCA and Kernel PCA

## 📚 Course Information
- **Course**: AH2179
- **Module**: 6
- **Project**: Dimensionality Reduction using PCA and Kernel PCA

## 🎯 Project Overview
This project explores dimensionality reduction techniques using **PCA** and **Kernel PCA**. The goal is to understand the effectiveness of various kernel functions in revealing underlying data structures and to assess their performance in comparison to traditional PCA.

## 🧪 Experiment Details

### Kernel Functions Tested
Different kernel PCA functions were used in comparison with PCA:
1. **Linear**
2. **Gaussian (RBF)**
3. **Polynomial**
4. **Sigmoid**

The **Gaussian kernel** provided the clearest cluster visualization, showing at least four clusters, while the **polynomial kernel** clustered all points together. Varying the `n_components` did not affect the visualizations, and modifying the polynomial range yielded no significant insights.

### 📈 Stability and Silhouette Scores
The following results were obtained for each kernel function:

| Method     | Stability Score | Silhouette Score |
|------------|-----------------|------------------|
| PCA        | 4.490175        | 0.485491        |
| Linear     | 4.487793        | -               |
| RBF        | 0.112908        | 0.517152        |
| Poly       | 0.258128        | 0.479314        |
| Sigmoid    | 0.177930        | NaN             |

There is no Silhouette Score for linear because it’s not a non-linear kernel transformation, and for sigmoid because the clustering results were not well-defined, leading to undefined or NaN values

### 🟢 Highlighted Result
- **Stability Index (L2 Distance) for Kernel RBF**: <span style="color:green">**0.10328911965205373**</span>

## 🔍 Key Findings

### Most Suitable Kernel for Dimensionality Reduction
Based on visualizations and scores, the **Gaussian kernel** was determined to be the most suitable for dimensionality reduction on dataset 1. Although the polynomial kernel had a high stability score, its clustering did not visually represent distinct groups.

### Comparison with PCA
Kernel PCA with the Gaussian kernel demonstrated better clustering than standard PCA, showing clearer separation. This suggests that kernel PCA with Gaussian is a better choice for this dataset.

### Reflection on Dimensionality Reduction Results
Due to the irregular distribution and non-convex shapes of clusters, standard PCA could not fully capture the data structure. Therefore, **Kernel PCA with the Gaussian kernel** was chosen for its ability to manage complex patterns in the data.

## 💡 Lessons Learned & Reflections
This assignment highlighted the importance of selecting appropriate dimensionality reduction techniques based on data complexity. Additionally, I learned about **Cosine** and **Jaccard similarity measures** as alternative similarity metrics, which I plan to explore further.

## 🔮 Future Applications in Transportation
The techniques learned could be applied to transportation issues, such as identifying clusters in high-dimensional data representing traffic flow patterns or analyzing multi-faceted transportation datasets for better infrastructure planning.

## 🌅 Visual Results

### 🗓️ PCA and Kernel PCA Comparison
<img src="https://github.com/user-attachments/assets/af10576c-f694-4b4a-9d1f-be6a06456976" width="550">

*Figure: Comparison of PCA and Kernel PCA visualizations using different kernel functions.*

### 📊 Stability Score Comparison Table
<img src="https://github.com/user-attachments/assets/46c88fef-2160-4968-8ec0-0292d9acd07c" width="200">

*Figure: Stability scores for each kernel function and PCA.*

### 📐 Silhouette Score Comparison
<img src= "https://github.com/user-attachments/assets/f5835cb8-dd99-4a14-8afe-ddac0f279944" width="200">

*Figure: Silhouette scores for each kernel function and PCA.*

---
