Ad Data Clustering & EDA
This project performs exploratory data analysis (EDA), outlier treatment, feature engineering, data preprocessing, and clustering (using both Hierarchical Clustering and KMeans) on a dataset containing digital advertising performance metrics.

📁 Dataset
Filename: Clustering+Clean+Ads_Data.xlsx

Contains information about ad size, platform, impressions, clicks, spend, revenue, device type, and derived metrics like CTR, CPC, CPM, etc.

🔧 Dependencies
Install the required Python libraries before running:

bash
Copy
Edit
pip install pandas numpy matplotlib seaborn scikit-learn scipy openpyxl
📊 Analysis Workflow
1. Loading and Exploring Data
Load data using pandas.

Check data types, shape, and missing values.

Ensure no duplicate records exist.

Generate summary statistics.

2. Univariate Analysis
Visualize distributions using boxplot and countplot.

Separate plots for numeric features like Impressions, Spend, Clicks, and categorical variables like Platform, Device Type, etc.

3. Bivariate Analysis
Explore relationships between numerical features and categorical ones using grouped boxplots.

4. Missing Value Treatment
Derive missing metrics using formulas:

CPM = (Spend / Impressions) × 1000

CPC = Spend / Clicks

CTR = (Clicks / Impressions) × 100

5. Outlier Treatment
Use the IQR method to detect and cap outliers.

Plot before and after treatment to validate the impact.

6. Feature Scaling
Apply Z-score normalization using scipy.stats.zscore.

7. Clustering Analysis
🔗 Hierarchical Clustering
Construct dendrogram using Ward’s linkage and Euclidean distance.

Visualize dendrogram and determine optimal number of clusters.

🔢 KMeans Clustering
Test K values from 1 to 10.

Evaluate inertia (WSS - Within-cluster Sum of Squares) to identify the elbow point.

📈 Output
Visualizations include boxplots, countplots, heatmaps, pairplots, and dendrograms.

Scaled dataset ready for clustering.

Optimal cluster count estimated visually from dendrogram and WSS plots.

💡 Notes
Missing values in CTR, CPC, and CPM are filled using formula-based techniques.

Outlier treatment avoids changing ad dimensions (Ad - Length, Ad- Width).

Ensure that Clustering+Clean+Ads_Data.xlsx is in the working directory.

📌 To Run
Just execute the Python file or run the cells if it's a Jupyter notebook. Ensure all packages are installed and data file is available.

