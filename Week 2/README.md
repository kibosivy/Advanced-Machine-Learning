# Spotify Song Clustering Analysis

This project performs an exploratory data analysis (EDA) and clustering analysis on a dataset of Spotify songs. The goal is to identify distinct groups of songs based on their audio features.

## Dataset

The dataset used in this analysis is **`ML_spotify_data.csv`**, which contains information about 10,000 songs, including:

- `name`: Song title  
- `artists`: Artist(s) of the song  
- `popularity`: Popularity score  
- `danceability`: Danceability score  
- `valence`: Positiveness of the song  
- `energy`: Perceptual measure of intensity and activity  
- `explicit`: Whether the song is explicit (0 or 1)  
- `key`: Key the track is in  
- `liveness`: Presence of an audience in the recording  
- `loudness`: Overall loudness in dB  
- `speechiness`: Presence of spoken words  
- `tempo`: Estimated tempo in BPM  

## Analysis Steps

1. **Data Loading and Initial Inspection**  
   - Load dataset into a pandas DataFrame.  
   - Check for missing values and duplicate rows.  

2. **Exploratory Data Analysis (EDA)**  
   - Visualized distributions of numerical features using histograms.  
   - Analyzed relationships between features using a correlation matrix heatmap.  
   - Identified outliers using box plots and handled them with Winsorization.  

3. **Preprocessing**  
   - Dropped non-numerical features (`name`, `artists`).  
   - Standardized numerical features using `StandardScaler`.  
   - Applied **Principal Component Analysis (PCA)** to reduce dimensionality while retaining most variance.  

4. **Clustering Methods**  
   - **K-Means Clustering**: Optimal clusters determined using the Elbow and Silhouette methods. Profiles analyzed.  
   - **Hierarchical Clustering**: Dendrogram plotted, Agglomerative Clustering applied, profiles analyzed.  
   - **DBSCAN**: Detected dense clusters and outliers. Profiles analyzed.  
   - **Gaussian Mixture Model (GMM)**: Modeled data as Gaussian mixtures, cluster profiles analyzed.  

## Results

The clustering analysis revealed distinct groups of songs based on their audio features.  
Detailed cluster characteristics and comparisons across algorithms are documented in the notebook.
