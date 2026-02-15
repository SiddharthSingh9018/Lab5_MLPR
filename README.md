## Report: Answers to Key Questions

#### 1. What are the common distance metrics used in distance based classification algorithms?
Metric 1: Euclidean distance
Why Euclidean?
Measures straight line distance between points; intuitive and widely used.
Effect
Sensitive to scale and outliers; works best when features are normalized.

Metric 2: Manhattan distance
Why Manhattan?
Measures sum of absolute differences; useful for grid like data.
Effect
Less sensitive to outliers; can handle high dimensional data better.

Metric 3: Minkowski distance
Why Minkowski?
Generalizes Euclidean and Manhattan; allows flexibility with parameter p.
Effect
Choice of p affects sensitivity to feature differences.

Metric 4: Cosine distance
Why Cosine?
Measures angle between vectors; useful for text and high dimensional data.
Effect
Ignores magnitude; focuses on orientation

#### 2. What are some real world applications of distance based classification algorithms?
Image recognition
Why distance based?
Compares pixel or feature vectors
Use 
Face, object, and handwriting recognition

Medical diagnosis
Why distance based?
Compares patient data to known cases.
Use:
Disease classification, anomaly detection.

Document classification
Why distance based?
Compares word frequency vectors.
Use:
Spam detection, topic categorization.

Recommender systems
Why distance-based?
Compares user/item profiles.
Use:
Product, movie, and content recommendations.

#### 3. Explain various distance metrics.
Euclidean distance
Why?
Straight-line distance; most common.
Effect:
Sensitive to scale, requires normalization.

Manhattan distance
Why?
Sum of absolute differences, robust to outliers.
Effect:
Useful for sparse or grid data.

Minkowski distance
Why?
Generalized metric; parameter p.
Effect:
Flexible, p=1 (Manhattan), p=2 (Euclidean).

Cosine distance
Why?
Measures angle; ignores magnitude.
Effect:
Good for text and high-dimensional data.

Mahalanobis distance
Why?
Accounts for feature correlation.
Effect:
Useful for multivariate data; requires covariance matrix.

#### 4. What is the role of cross validation in model performance?
Role: Model evaluation
Why cross validation?
Splits data into training and testing sets multiple times.
Effect:
Provides unbiased estimate of model performance; reduces overfitting risk.

Role: Hyperparameter tuning
Why?
Tests different parameter values.
Effect
Helps select best model settings improves generalization.

Role: Model selection
Why?
Compares multiple algorithms.
Effect:
Identifies most suitable model for the task.

#### 5. Explain variance and bias in terms of KNN?
Variance
Why variance?
Measures sensitivity to training data changes.
Effect:
KNN with low k has high variance; model changes with new data.

Bias
Why bias?
Measures error due to model assumptions.
Effect:
KNN with high k has high bias; predictions are averaged, less sensitive to local structure.

Trade-off
Why trade-off?
Balance between bias and variance.
Effect:
Optimal k minimizes both; too low k overfits, too high k underfits.
# Face Detection and Clustering Lab

## Aim
This lab demonstrates face detection using OpenCV and clustering of detected faces based on color features (hue and saturation) using KMeans. The goal is to understand distance-based classification and clustering techniques in computer vision.

## Methodology
- **Face Detection:**
  - Used Haar Cascade classifier to detect faces in an image (`Plaksha_Faculty.jpg`).
  - Converted the image to grayscale for detection.
  - Drew rectangles and labeled detected faces.
- **Feature Extraction:**
  - Converted detected face regions to HSV color space.
  - Extracted mean hue and saturation for each face.
- **Clustering:**
  - Applied KMeans clustering (k=2) on the hue-saturation features.
  - Visualized clusters and centroids.
- **Template Matching:**
  - Detected and extracted features from a template image (`Dr_Shashi_Tharoor.jpg`).
  - Predicted its cluster assignment.

## Key Findings
- Face detection works reliably with proper cascade file loading and parameter tuning.
- Clustering based on color features can group similar faces, but is sensitive to lighting and color variations.
- Template matching allows classification of new faces into existing clusters.

## Conclusions
- Distance-based methods (like KNN, KMeans) are effective for classification and clustering when features are well-chosen.
- Proper preprocessing and parameter selection are crucial for robust results.
- Visualizations help interpret and validate clustering/classification outcomes.


## Visualizations
Below are the actual outputs and screenshots from the lab:

### Screenshot: Detected Faces (Group Photo)
![Detected Faces](Screenshot%202026-02-15%20221501.png)

### Screenshot: Clustered Faces by Hue and Saturation
![Clustered Faces by Hue and Saturation](Screenshot%202026-02-15%20224438.png)

### Screenshot: Scatter Plot of Face Clusters
![Scatter Plot of Face Clusters](Screenshot%202026-02-15%20224446.png)

### Screenshot: Face Clusters and Template Assignment
![Face Clusters and Template Assignment](Screenshot%202026-02-15%20224506.png)

### Source Images
#### Dr. Shashi Tharoor
![Dr. Shashi Tharoor](images/Dr_Shashi_Tharoor.jpg)

#### Plaksha Faculty
![Plaksha Faculty](images/Plaksha_Faculty.jpg)


## How to Run
1. Install requirements: `pip install opencv-python numpy matplotlib scikit-learn`
2. Place the required images in the working directory.
3. Run the Jupyter notebook step by step.
4. Review the visual outputs and report answers at the end of the notebook.


## Author
Siddharth Singh
CSAI ug24 0096
