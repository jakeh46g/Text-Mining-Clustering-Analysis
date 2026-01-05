# Text Mining & Clustering Analysis

## Overview
Natural Language Processing (NLP) project that analyzes airline customer feedback using text mining and hierarchical clustering techniques to automatically categorize customer complaints and identify common themes.

## Objective
- Extract meaningful insights from unstructured customer feedback
- Identify key complaint themes using text mining
- Automatically cluster similar customer comments
- Enable better customer service resource allocation through complaint categorization

## Business Value
This analysis helps airline management:
- **Route complaints to appropriate teams** (flight staff vs. gate agents vs. baggage handlers)
- **Identify recurring issues** (rude staff, damaged bags, flight delays)
- **Prioritize customer service improvements** based on complaint frequency
- **Automate initial complaint triage** saving time and improving response speed

## Technologies Used
- **Python**: Core programming language
- **scikit-learn**: Text vectorization, clustering algorithms
- **pandas**: Data manipulation
- **NumPy**: Numerical operations
- **matplotlib**: Data visualization
- **scipy**: Hierarchical clustering and dendrogram generation
- **Regular expressions (re)**: Text preprocessing

## Dataset
- **Source**: airlinetweets.csv (airline customer feedback)
- **Format**: Text comments from airline customers
- **Size**: 36 customer comments
- **Content**: Customer complaints about airline service including baggage issues, staff behavior, flight problems, and gate operations

## Methodology

### 1. Data Preprocessing
- Text cleaning: Removed special characters and punctuation using regex
- Normalization: Converted all text to lowercase
- Stop word removal: Filtered out common English words using scikit-learn's built-in stop words list

### 2. Feature Extraction
- **Term-Document Matrix**: Converted text to binary matrix representation
- **Top Features**: Extracted top 5 most frequent terms: 'agent', 'bag', 'flight', 'gate', 'rude'
- **Binary Encoding**: Used presence/absence (1/0) of terms rather than frequency counts

### 3. Hierarchical Clustering
- **Algorithm**: Agglomerative Clustering with Ward linkage
- **Distance Metric**: Euclidean distance
- **Number of Clusters**: 4 optimal clusters identified
- **Visualization**: Dendrogram showing hierarchical relationships

### 4. Cluster Interpretation
The algorithm successfully identified 4 distinct complaint categories:

- **Cluster 0 - Flight Operations**: Comments about flight delays, equipment problems, onboard service
- **Cluster 1 - Gate Agent Issues**: Complaints specifically about rude or unhelpful gate agents
- **Cluster 2 - Baggage Handling**: Lost, damaged, or mishandled luggage complaints
- **Cluster 3 - Miscellaneous**: General complaints and mixed issues

## Key Findings

### Top 5 Complaint Terms
1. **Agent** - Most frequently mentioned, indicating staff interaction issues
2. **Bag** - Baggage problems are a major concern
3. **Flight** - Flight operations and delays
4. **Gate** - Gate operations and boarding issues
5. **Rude** - Customer service quality concerns

### Clustering Results
- Successfully separated baggage complaints from staff complaints
- Distinguished between gate agent issues vs. flight attendant issues
- Identified actionable categories for management intervention

### Business Insights
- **Staff Training Priority**: High frequency of "rude" and "agent" suggests need for customer service training
- **Baggage Handling**: Dedicated cluster indicates systematic issues with luggage handling
- **Departmental Routing**: Complaints can be automatically routed to:
  - Gate operations team
  - In-flight service team  
  - Baggage handling department
  - General customer service

## Visualization
The dendrogram clearly shows the hierarchical structure of complaints, with distinct branches representing:
- Baggage-related complaints clustering together
- Staff behavior complaints forming a separate group
- Flight operations issues in another distinct cluster

## Dataset

The `airlinetweets.csv` file contains 36 customer complaints covering issues such as:
- Damaged luggage and baggage fees
- Rude or unhelpful staff (gate agents and flight attendants)
- Flight delays and equipment problems
- Boarding issues and gate operations
- Wet or damaged belongings

**Important modifications for local execution:**

1. **Remove Google Colab cells**: Comment out or delete these cells at the beginning:
   ```python
   from google.colab import drive
   drive.mount('/content/drive')
   ```

2. **Update data path**: Change the file loading line from:
   ```python
   with open("/content/drive/MyDrive/Colab Notebooks/data/airlinetweets.csv", "r", encoding="utf-8") as file:
   ```
   to:
   ```python
   with open("airlinetweets.csv", "r", encoding="utf-8") as file:
   ```

## Skills Demonstrated

### Natural Language Processing
- Text preprocessing and cleaning
- Stop word removal
- Term frequency analysis
- Document vectorization

### Machine Learning
- Unsupervised learning (clustering)
- Hierarchical clustering
- Agglomerative clustering with Ward linkage
- Distance metric selection

### Data Analysis
- Pattern recognition in text data
- Cluster interpretation and labeling
- Business insight extraction

### Python Libraries
- **scikit-learn**: CountVectorizer, AgglomerativeClustering
- **scipy**: Hierarchical clustering and dendrograms
- **pandas**: Data manipulation
- **matplotlib**: Visualization

## Practical Applications

This analysis framework can be applied to:
- Customer service automation
- Social media monitoring
- Product review analysis  
- Help desk ticket categorization
- Email routing and prioritization
- Quality assurance feedback analysis

## Author
**Jacob Hefele**
- [LinkedIn](https://www.linkedin.com/in/jacob-hefele46)
- [GitHub](https://github.com/jakeh46g)
