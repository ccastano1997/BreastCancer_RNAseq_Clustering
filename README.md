# BreastCancer_RNAseq_Clustering

This project explores gene expression patterns in breast cancer using K-means clustering and analyzes the resulting clusters in the context of clinical data.

## Dataset

The dataset used in this project is GSE113863, which contains targeted RNA-seq data from 483 breast cancer samples. It includes a 72-gene panel and associated clinical information.

* **Source:** Gene Expression Omnibus (GEO) - [https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE113863](https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE113863)

## Analysis

The analysis involved the following steps:

1. **Data Loading:** The normalized gene expression data was loaded from the `GSE113863_dwd_normalized_std_expression.csv` file.
2. **Clustering:** K-means clustering was performed to group the samples based on their gene expression profiles. The elbow method and silhouette analysis were used to explore the optimal number of clusters (k).
3. **Cluster Analysis:**
   * **PAM50 Comparison:** The cluster assignments were compared to the PAM50 molecular subtypes to assess their agreement and identify discrepancies.
   * **Clinical Correlation:** The clusters were analyzed in the context of clinical data, including distant metastasis-free survival (DMFS) time. ANOVA tests and Tukey's HSD post-hoc tests were used to identify significant differences between the clusters.
   * **Differential Gene Expression:** Differentially expressed genes between the clusters were identified using ANOVA tests and visualized using heatmaps and volcano plots.

## Findings

* **Optimal k:** The elbow method and silhouette analysis suggested k=2 or k=3 as potential optimal values for the number of clusters.
* **PAM50 Agreement:** The clusters showed moderate agreement with the PAM50 subtypes, indicating that the clustering captured some of the known molecular subtypes of breast cancer.
* **DMFS Analysis:** Significant differences in DMFS time were observed between the clusters, suggesting potential prognostic value.
* **Gene Expression:** Several genes were identified as differentially expressed between the clusters, providing insights into the molecular characteristics of each cluster.

## Future Directions

This project can be further extended by:

* **Pathway Analysis:** Perform pathway enrichment analysis (e.g., GO, KEGG) to identify biological pathways associated with each cluster.
* **Deeper Clinical Analysis:** Explore the relationship between clusters and other clinical variables, such as tumor grade and stage.
* **Survival Analysis:** Conduct more detailed survival analysis (e.g., Kaplan-Meier curves, Cox regression) to assess the prognostic value of the clusters.
* **Validation:**  Validate the findings on an independent breast cancer dataset.
* **Literature Search:** Research the top differentially expressed genes to understand their roles in breast cancer and their potential as drug targets.

This project demonstrates the application of unsupervised machine learning techniques to analyze gene expression data and identify potential subtypes of breast cancer with different clinical outcomes.
