## 🚀 Project Workflow
I have used Mall data for this project which is available and accessable to anyone.
### 1. Exploratory Data Analysis (EDA)
* Utilized `seaborn.pairplot` to visualize pairwise relationships and distributions across numerical features.
* Applied categorical color mapping (`hue`) to inspect natural groupings visually before clustering.

### 2. Data Preprocessing & Scaling
* Handled object/text data types to ensure all input variables were strictly numeric.
* Standardized features using `StandardScaler` to ensure distance metrics were not skewed by columns with larger scales (e.g., income vs. age).

### 3. Finding Optimal Clusters (The Elbow Method)
* Iterated through a range of clusters (k = 1 to 10) to calculate the **Within-Cluster Sum of Squares (WCSS / Inertia)** using `scikit-learn`.
* Plotted the WCSS curve to identify the inflection point ("elbow joint") to mathematically select the best number of clusters (k = 5).

### 4. Model Training & Prediction
* Trained the final K-Means model with k = 5 clusters and `init="k-means++"` for optimized initial centroid placement.
* Generated target cluster labels using `.fit_predict()`.

### 5. Cluster Profiling
* Aggregated the data by grouping by the newly assigned clusters.
* Computed the statistical `mean` across numeric columns to build behavioral profiles for each of the 5 consumer/data segments.

## 🛠️ Tech Stack & Tools
* **Language:** Python
* **Libraries:** 
  * `pandas` & `numpy` (Data manipulation & cleaning)
  * `scikit-learn` (StandardScaler & KMeans clustering)
  * `seaborn` & `matplotlib` (Data visualization & elbow curve plotting)

## 📊 Key Results
* Successfully isolated **5 distinct segments** within the dataset.
* Created an automated script that securely filters numeric types to prevent aggregation errors (`agg function failed`) during profile generation.

## 🏃 How to Run the Project
1. Clone this repository:
   ```bash
   git clone https://github.com
   ```
2. Install dependencies:
   ```bash
   pip install pandas numpy scikit-learn seaborn matplotlib
   ```
3. Run the Jupyter Notebook or Python script to train the model and view the resulting cluster profiles.
