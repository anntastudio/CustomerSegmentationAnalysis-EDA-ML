# CustomerSegmentationAnalysis-EDA-ML
### Project background
This project delivers a customer segmentation solution that transforms how a supermarket understands and engages its customer base. By applying machine learning to analyse purchasing behavior, demographics, and engagement patterns, the solution identifies 4 distinct customer segments. This enables the marketing team to execute targeted campaigns, optimise promotional strategies, improve retention rates, and drive revenue growth through data-driven personalisation.

### Business challenges
* The business struggles to understand diverse customer needs with a one-size-fits-all approach
* Marketing campaigns often lack personalisation, resulting in low conversion rates
* Resources are inefficiently allocated across customer groups with varying profitability
* Customer retention strategies are not tailored to specific behavioral patterns

### Project Objectives
Primary: Identify and profile customer segments to drive:
* Targeted marketing strategies
* Product-customer alignment in sales
* Segment-informed product development
* Personalised customer retention programs

Secondary:
* Executive visibility into customer insights
* Enhanced business profitability
<br>

### Findings and Recommendation
<img width="1760" height="367" alt="image" src="https://github.com/user-attachments/assets/cd1df68e-8cd4-4cc6-9f74-7e437affca40" />

Four (04) is the optimal number of clusters, faily evenly distributed ranging from 490 to 600 customers each.

| Cluster | Income | Age | Family Size | 
|------|------|------|------|
| 0 | middle to high income | 40-80 years old | up to 4 people, with kids | 
| 1 | low income | relatively younger, between 25 and 60| mostly 2-3 people per household |
| 2 | high income | 30-75 years old | mostly single or couples with no kids |
| 3 | low to middle income | 40-80 years old | larger family, up to 5 people |


<img width="998" height="367" alt="image" src="https://github.com/user-attachments/assets/e05dd4b7-02ac-42d2-8e9c-a9c7b7496a4d" />

A look into customers' responses to promotions

| Cluster | Response to Promotion | Recommendation |
|------|------|------|
| 0 | minimal engagement to promotional offers, moderate number of purchases, 3-4 deals | avoid over promotion, stick to traditional marketing channels and encourage volume, such as buy 2 get 1 free | 
| 1 | not engage with promotions, low purchase volume, average 2 deals | low value group, neither sensitive to sales nor high purchasers. Based on younger demographic, run social media campaigns or kids friendly experiences | 
| 2 | most responsive to promotions, but purchases the least, possibly bargain hunters | focus on quality or premium products on lifestyle channels
| 3 | the highest value segment who occasionally engage with promotions | run promotions on bulk buying options, offer loyalty programs |



<br>

### Methodology
* Data source: extracts in csv format
* Technology used: Python 3.12.2, Pandas, Numpy, Scikit-learn, Matplotlib, Seaborn, Yellowbrick, PCA, Agglomerative Clustering, Label Encoding, StandardScaler, Google Colab, Jupyter Notebook
* Data structure (raw data)
<img width="370" height="606" alt="image" src="https://github.com/user-attachments/assets/4d16dcb7-1c51-43a4-b3ff-c7b53f5f7eae" />
<br>

* Process and techniques

  Exploratory Data Analysis (EDA)
    * Statistical analysis of 29 customer features across 2,240 data points
    * Distribution analysis and outlier detection
    * Feature correlation and relationship exploration
    * Multi-dimensional data visualization (2D/3D scatter plots, box plots, swarm plots, KDE plots)
    * Data quality assessment and missing value treatment
  
  Machine Learning (ML)
    * Feature Engineering: Created 7+ derived features (Age, Spent, Family_Size, Is_Parent, etc.)
    * Data Preprocessing: Label Encoding, Standard Scaling, outlier removal
    * Dimensionality Reduction: PCA (Principal Component Analysis) for feature reduction
    * Unsupervised Learning: Agglomerative Clustering with optimal cluster selection
    * Model Evaluation: Elbow Method for determining optimal k-value
    * Cluster Analysis: Profiling and interpreting customer segments
