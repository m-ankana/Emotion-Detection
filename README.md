EMOTION DETECTION

**Features and Workflow
1. Importing Libraries

Utilizes essential Python libraries such as cv2, os, numpy, and sklearn for data handling, image processing, and dataset splitting.

2. Directory Setup

The code defines paths to directories containing images for seven emotional categories (** change the path accordingly):
Angry
Disgust
Fear
Happy
Neutral
Sad
Surprise

3. Image Preprocessing

Each image is:

Loaded from the respective directory using cv2.imread.
Converted to grayscale using cv2.cvtColor for simplicity and reduced computational load.
Resized to a fixed dimension of 100x100 pixels for uniformity.
Appended to the images list, while the corresponding emotion category is added to the targets list.
Exceptions during file processing are handled gracefully with error messages.

4. Dataset Preparation

Images (X) and labels (Y) are converted to NumPy arrays for efficient numerical operations.
The data is split into training (80%) and testing (20%) subsets using train_test_split.

5. Data Normalization

Images are reshaped to include a channel dimension ((100, 100, 1)) and normalized to the range [0, 1] for compatibility with deep learning models.

6. Label Encoding

Emotion labels are encoded into numerical values using LabelEncoder for compatibility with machine learning models.

7. Model Readiness

The preprocessed and normalized data is ready for use in machine learning or deep learning models, including convolutional neural networks (CNNs).

Code Highlights

Error Handling: Ensures that issues with reading or processing specific images do not interrupt the pipeline.
Scalability: Supports multiple emotion categories and can be extended with additional preprocessing techniques.
Standardized Dimensions: Ensures uniformity in image size and grayscale format, simplifying downstream tasks.
Possible Enhancements

Add data augmentation techniques to increase dataset diversity (e.g., rotation, flipping, zooming).
Integrate a visualization module to inspect preprocessed images and distribution of emotion categories.
Include a sample deep learning model to demonstrate the usage of the processed data.

Requirements

Python 3.x
Libraries: OpenCV, NumPy, scikit-learn

RESULT:
The accuracy of the project is 89%.
