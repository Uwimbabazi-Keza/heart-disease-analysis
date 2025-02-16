# Heart disease analysis

## Background

The [Heart Disease Dataset](https://archive.ics.uci.edu/dataset/45/heart+disease) contains 303 instances with 13 features each, aimed at classifying the presence of heart disease. The primary goal is to distinguish the presence (values 1-4) from the absence (value 0) of heart disease.

## Attributes
- **age**: Age
- **sex**: Gender (1 = male, 0 = female).
- **cp**: Chest pain type (1 = typical angina, 2 = atypical angina, 3 = non-anginal pain, 4 = asymptomatic).
- **trestbps**: Resting blood pressure (in mm Hg on admission to the hospital).
- **chol**: Serum cholesterol level in mg/dl.
- **fbs**: Fasting blood sugar > 120 mg/dl (1 = true, 0 = false).
- **restecg**: Resting electrocardiographic results (0 = normal, 1 = having ST-T wave abnormality, 2 = showing probable or definite left ventricular hypertrophy).
- **thalach**: Maximum heart rate achieved.
- **exang**: Exercise induced angina (1 = yes, 0 = no).
- **oldpeak**: ST depression induced by exercise relative to rest.
- **slope**: The slope of the peak exercise ST segment (1 = upsloping, 2 = flat, 3 = downsloping).
- **ca**: Number of major vessels colored by fluoroscopy (0-3).
- **thal**: Thalassemia (3 = normal, 6 = fixed defect, 7 = reversible defect).
- **num**: Presence of heart disease (0 = absence, 1-4 = presence).

## Analysis Process

### Data Loading and Preprocessing:
- Loaded the dataset into a Pandas DataFrame.
- Used Exploratory Data Analysis (EDA) to understand the distribution of variables and handle missing values. 

### Clustering and GMM:
- Applied K-means clustering, hierarchical clustering, and DBSCAN to cluster patients based on their medical history.
- Visualized clusters using PCA and t-SNE.
- Used Gaussian Mixture Models (GMMs) to identify risk factors associated with heart disease.

### Evaluation:
- Metrics included Silhouette score and Davies-Bouldin index to compare the performances.

### Conclusion:
- **Hierarchical Clustering** has the highest Silhouette Score (0.181853), which shows it is the best-defined clusters
- **DBSCAN** has the lowest Davies-Bouldin Index (1.175540), suggesting good cluster quality but weaker with cluster definition
- **K-means** and **GMM** are less effective in defining clusters and maintaining cluster quality compared to Hierarchical Clustering and DBSCAN.

Therefore, Hierarchical Clustering is a stronger choice which proves to be the best balance between cluster definition and quality for this dataset.