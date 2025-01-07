# Siamese-CNN-for-Change-Detection-on-Satellite-Images
This repository contains the implementation of a Siamese Convolutional Neural Network (CNN) model for detecting changes in satellite images. The model has been trained on the WHU RS Change Detection Dataset and outputs binary change maps that identify regions of significant changes between pre-change and post-change images.

Features
Model Architecture: The Siamese CNN uses two convolutional branches to independently process pre-change and post-change images. A feature fusion mechanism is applied to compute differences and generate a binary change map.
Dataset: Trained on the WHU RS Change Detection Dataset, which contains annotated high-resolution satellite images for pixel-level change detection tasks.
Output: Produces binary change maps highlighting areas of interest.
Applications: Useful for urban monitoring, environmental studies, disaster management, and infrastructure assessment.

Model Overview
Siamese CNN Architecture
The Siamese CNN consists of:

* Two identical convolutional branches to extract spatial features from pre-change and post-change images.
* Shared weights between the branches to ensure consistent feature extraction for both inputs.
* Feature difference computation: Combines the feature maps from both branches to capture changes.
* Binary classifier to output a pixel-wise binary change map.

Dataset
WHU RS Change Detection Dataset
The WHU RS Change Detection Dataset is used for training and evaluation:

Dataset contents:
* Satellite image pairs (pre-change and post-change).
* Ground truth binary masks for changes.

Applications:
* Monitoring urban growth.
* Tracking deforestation and environmental degradation.
* Assessing disaster-affected areas.
* For detailed information, visit the WHU RS Dataset Page.

Results
Evaluation Metrics: Model performance is measured using metrics such as Precision, Recall, F1-Score, and Intersection over Union (IoU).


Here’s a draft for the README file for your Siamese CNN model trained on the WHU RS Change Detection Dataset:

Siamese CNN for Change Detection on Satellite Images
This repository contains the implementation of a Siamese Convolutional Neural Network (CNN) model for detecting changes in satellite images. The model has been trained on the WHU RS Change Detection Dataset and outputs binary change maps that identify regions of significant changes between pre-change and post-change images.

Features
Model Architecture: The Siamese CNN uses two convolutional branches to independently process pre-change and post-change images. A feature fusion mechanism is applied to compute differences and generate a binary change map.
Dataset: Trained on the WHU RS Change Detection Dataset, which contains annotated high-resolution satellite images for pixel-level change detection tasks.
Output: Produces binary change maps highlighting areas of interest.
Applications: Useful for urban monitoring, environmental studies, disaster management, and infrastructure assessment.
Model Overview
Siamese CNN Architecture
The Siamese CNN consists of:

Two identical convolutional branches to extract spatial features from pre-change and post-change images.
Shared weights between the branches to ensure consistent feature extraction for both inputs.
Feature difference computation: Combines the feature maps from both branches to capture changes.
Binary classifier to output a pixel-wise binary change map.
Dataset
WHU RS Change Detection Dataset
The WHU RS Change Detection Dataset is used for training and evaluation:

Dataset contents:
Satellite image pairs (pre-change and post-change).
Ground truth binary masks for changes.
Applications:
Monitoring urban growth.
Tracking deforestation and environmental degradation.
Assessing disaster-affected areas.
For detailed information, visit the WHU RS Dataset Page.

Results
Evaluation Metrics: Model performance is measured using metrics such as Precision, Recall, F1-Score, and Intersection over Union (IoU).
Sample Output:
Pre-Change Image	Post-Change Image	Change Map
Installation
Clone the repository:
bash
Copy code
git clone https://github.com/yourusername/siamese-cnn-change-detection.git
cd siamese-cnn-change-detection
Install dependencies:
bash
Copy code
pip install -r requirements.txt
Usage
Training the Model
Prepare the Dataset:
Download the WHU RS Change Detection Dataset.
Place the dataset in the data/ directory.
Train the Model:
bash
Copy code
python train.py --config config.yaml
Testing the Model
Test the model on satellite image pairs:

bash
Copy code
python test.py --pre_image path/to/pre_image.png --post_image path/to/post_image.png --output path/to/output.png
Requirements
Python 3.8+
TensorFlow or PyTorch (depending on your implementation)
Other dependencies (listed in requirements.txt)
Results Visualization
Visualize the results by overlaying the change map on the original images. Use the script:

bash
Copy code
python visualize_results.py --pre_image path/to/pre_image.png --post_image path/to/post_image.png --change_map path/to/output.png
Acknowledgments
Thanks to the creators of the WHU RS Change Detection Dataset.
The Siamese CNN architecture is inspired by research in deep learning for change detection.
