# Customer Segmentation Analysis Using K-Means Clustering

## Overview
Unsupervised learning analysis to segment customers by age and income demographics, identifying optimal market segments for targeted business strategies.

## Objective
- Identify distinct customer segments within demographic data
- Determine optimal number of clusters using silhouette analysis
- Visualize customer groupings for strategic planning

## Technologies Used
- **Python**: Core programming language
- **scikit-learn**: K-means clustering, preprocessing, metrics
- **pandas**: Data manipulation and analysis
- **matplotlib/seaborn**: Data visualization
- **scipy**: Statistical analysis (z-score normalization)

## Methodology

### 1. Data Preprocessing
- Applied z-score normalization to ensure equal feature weighting
- Standardized Age and Income variables to prevent income from dominating clustering due to scale differences

### 2. Optimal Cluster Selection
- Evaluated 2-6 clusters using silhouette score analysis
- **Results:**
  - 2 clusters: 0.478
  - 3 clusters: 0.417
  - 4 clusters: 0.444
  - **5 clusters: 0.490** (optimal)
  - 6 clusters: 0.480

### 3. Model Training
- Implemented K-means with 3 clusters for business interpretability
- Used automated initialization (`n_init='auto'`)
- Focused on Age and Income features for clear visualization

### 4. Visualization
- Created scatter plots showing age vs. income segmentation
- Color-coded clusters for easy identification of customer groups

## Key Findings
- Successfully identified 3 distinct customer segments based on age and income patterns
- Silhouette analysis revealed 5 clusters provided optimal mathematical separation
- Chose 3-cluster model for practical business application and interpretability
- Clear demographic groupings emerged suitable for targeted marketing strategies

## Dataset
- **Source**: nestegg.csv (sample customer data)
- **Features**: 
  - Age: Customer age in years
  - Income: Annual income
- **Size**: 45 customer records

## Usage

### Option 1: Run in Google Colab (Recommended)
Click the "Open in Colab" badge at the top of the notebook to run this analysis in your browser with no setup required.

1. Click the Colab badge in `K_Means_Clustering.ipynb`
2. Upload your own `nestegg.csv` file when prompted, or use the sample data
3. Run all cells

### Option 2: Run Locally
To run this notebook locally, you'll need to modify the data loading section since it's configured for Google Colab.
```bash
# Clone repository
git clone https://github.com/jakeh46g/K-Means-Clustering-Analysis
cd K-Means-Clustering-Analysis

# Install required packages
pip install pandas numpy scikit-learn matplotlib seaborn scipy jupyter

# Start Jupyter notebook
jupyter notebook
```

**Then modify the notebook:**
- Remove or comment out the Google Drive mount cells
- Change the data loading path from:
```python
  df = pd.read_csv('/content/drive/MyDrive/Colab Notebooks/data/nestegg.csv')
```
  to:
```python
  df = pd.read_csv('nestegg.csv')
```

### Run Locally
```bash
# Clone repository
git clone https://github.com/jakeh46g/K-Means-Clustering-Analysis
cd K-Means-Clustering-Analysis

# Install required packages
pip install pandas numpy scikit-learn matplotlib seaborn scipy

# Open Jupyter notebook
jupyter notebook K_Means_Clustering.ipynb
```

## Skills Demonstrated
- **Unsupervised Machine Learning**: K-means clustering algorithm
- **Feature Engineering**: Data normalization and scaling
- **Model Evaluation**: Silhouette score analysis for optimal cluster selection
- **Data Visualization**: Matplotlib and Seaborn for insights presentation
- **Statistical Analysis**: Z-score standardization

## Future Improvements
- Incorporate additional demographic features (location, education level, occupation)
- Compare with alternative clustering algorithms (DBSCAN, hierarchical clustering)
- Develop detailed customer profiles for each segment
- Implement elbow method as additional validation
- Build recommendation engine based on segment characteristics
- Add interactive visualizations using Plotly

## Author
**Jacob Hefele**
- [LinkedIn](https://www.linkedin.com/in/jacob-hefele46)
- [GitHub](https://github.com/jakeh46g)

## License
This project is available for educational and portfolio purposes.
