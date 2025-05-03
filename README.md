# Global Development and Prosperity Indices Analysis

## Project Overview
This project applies unsupervised machine learning techniques to analyze the 2023 Global Country Development & Prosperity Index data. The core objective was to determine if countries can be naturally grouped into distinct developmental clusters based on continuous prosperity metrics, and to explore whether these clusters correlate with geographic regions.

## Dataset
The analysis utilizes the 2023 Legatum Prosperity Index data, which contains 14 features for 167 countries:
- Overall average score across all indicators
- Specialized indices covering:
  - Safety and security
  - Personal freedom
  - Governance
  - Social capital
  - Investment environment
  - Enterprise conditions
  - Market access and infrastructure
  - Economic quality
  - Living conditions
  - Health
  - Education
  - Natural environment

Each numerical score is normalized to fall between 0 and 100.

## Technical Skills Demonstrated
This project showcases proficiency in:

1. **Data Exploration and Preprocessing**
   - Identifying and handling outliers
   - Assessing multicollinearity between features
   - Feature scaling using StandardScaler

2. **Dimensionality Reduction**
   - Principal Component Analysis (PCA) for visualization
   - Analysis of variance explained by principal components
   - Interpretation of component coefficients and contributions

3. **Unsupervised Clustering Methods**
   - K-means clustering
   - Hierarchical Agglomerative Clustering (HAC) with Ward linkage
   - DBSCAN (Density-Based Spatial Clustering of Applications with Noise)
   - Hyperparameter tuning and evaluation

4. **Advanced Data Visualization**
   - Interactive choropleth maps using Plotly
   - Scatter plots in principal component space
   - Combined multi-panel visualizations

5. **Statistical Analysis**
   - Correlation analysis
   - Distribution assessment
   - Cluster validation

## Key Findings

- **Robust Three-Cluster Pattern**: Both K-means and Hierarchical Agglomerative Clustering independently identified similar three-cluster patterns in the data, confirming the robustness of the clustering results.

- **Geographic Correlation**: The identified clusters strongly correlate with geographic patterns typically associated with development levels:
  - Highest-ranked cluster: North America, Western Europe, and Oceania (with Japan, South Korea, and Chile)
  - Intermediate cluster: Eastern Europe, Asia, South and Central America (with parts of North Africa and South Africa)
  - Lowest-ranked cluster: Most of Africa and portions of Asia and South America

- **Quasi-One-Dimensional Data**: The analysis revealed that the data is nearly one-dimensional, with the first principal component explaining over 74% of total variance. This component correlates almost perfectly with the average score across all indices.

- **Hierarchical Fine Structure**: HAC analysis uncovered potentially interesting sub-clusters, such as the distinction between Nordic countries versus other European countries, revealing nuanced differences in development patterns.

- **DBSCAN Limitations**: The density-based DBSCAN method failed to produce meaningful clusters across the examined hyperparameter range, suggesting this approach is not well-suited for this particular dataset's structure.

## Limitations and Future Work

The analysis has several limitations that could be addressed in future work:

- The data represents only a single year (2023), and incorporating multiple years would allow for examining temporal patterns and robustness.

- The data comes from a single non-governmental source. Incorporating data from other sources such as the IMF and World Bank would strengthen the robustness of findings.

- The identified clusters largely reproduce conventional development patterns, which may reflect underlying biases in the data itself.

- Future analyses could focus on the fine structure identified in the HAC analysis to explore sub-regional development patterns and potentially inform targeted policy interventions.

## Technologies Used
- Python
- NumPy
- Pandas
- Matplotlib
- Seaborn
- Plotly
- Scikit-learn