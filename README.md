# Document Similarity Analysis using PySpark and Locality-Sensitive Hashing (LSH)

My name is Hamed Davoodi, matriculation number 11267A. I utilized a PySpark DataFrame to analyze document similarity through MinHash and Locality-Sensitive Hashing (LSH). This project explores the application of scalable techniques for document similarity analysis using large datasets. Below is a detailed outline of the process I implemented in this notebook.

## Project Workflow

### 1. Environment Setup
   - Installed required packages and configured the environment for PySpark.
   
### 2. Data Retrieval
   - Utilized Kaggle API key to download the LinkedIn dataset from Kaggle.

### 3. Initialize Spark Session
   - Configured and started a Spark session to enable distributed data processing.

### 4. Load Dataset
   - Loaded the LinkedIn dataset into a distributed PySpark DataFrame format for efficient processing.

### 5. Adjust Partitioning
   - Repartitioned the dataset to enhance scalability and optimize processing speed in distributed environments.

### 6. Filter and Preprocess
   - Excluded non-English language entries from the dataset.
   - Cleaned and preprocessed text data, including removing special characters and lowering the text case.

### 7. Tokenize Data
   - Split the documents into tokens for further processing.

### 8. Generate N-Grams
   - Created N-Gram sequences from the tokenized data to capture more contextual patterns.

### 9. Zero-One Features
   - Applied one-hot encoding to convert N-Grams into feature vectors for each document.

### 10. MinHash Application
   - Reduced the dimensionality of the feature vectors by applying MinHash, a technique used to approximate the Jaccard similarity.

### 11. Band Creation
   - Segmented MinHash signatures into bands for further hashing.

### 12. Bucketing
   - Used Python’s default hashing function to hash the bands into buckets, allowing us to identify candidate pairs of similar documents.

### 13. Similarity Check
   - Performed Jaccard similarity calculation on the candidate pairs to confirm document similarity.
## Dataset
The dataset is sourced from the LinkedIn dataset on Kaggle, consisting of millions of user profiles and text-based features. This dataset is ideal for testing large-scale document similarity techniques.
