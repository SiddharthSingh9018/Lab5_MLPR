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

### Detected Faces (Group Photo)
![Detected Faces](../Plaksha_Faculty_faces.png)

### Clustered Faces by Hue and Saturation
![Clustered Faces by Hue and Saturation](../clustered_faces_hue_saturation.png)

### Scatter Plot of Face Clusters
![Scatter Plot of Face Clusters](../scatter_plot_face_clusters.png)

### Template Image Cluster Assignment
![Template Image Cluster Assignment](../template_image_cluster_assignment.png)

### Face Clusters and Template Assignment
![Face Clusters and Template Assignment](../face_clusters_and_template_assignment.png)

### Source Images
#### Dr. Shashi Tharoor
![Dr. Shashi Tharoor](../Dr_Shashi_Tharoor.jpg)

#### Plaksha Faculty
![Plaksha Faculty](../Plaksha_Faculty.jpg)

---

## How to Run
1. Install requirements: `pip install opencv-python numpy matplotlib scikit-learn`
2. Place the required images in the working directory.
3. Run the Jupyter notebook step by step.
4. Review the visual outputs and report answers at the end of the notebook.

---

## Author
Siddharth Singh
CSAI ug24 0096
