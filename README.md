<h2>Crops Disease Dectection Model</h2>


# Crop Disease Detection using YOLO and Custom Data Augmentation

![image](https://github.com/user-attachments/assets/673954ad-c427-4c4f-8531-838fa840468d)


## Project Overview
This project explores machine learning techniques for detecting crop diseases in images using the YOLO model. The goal is to develop an accurate and efficient model to identify different diseases across various crops, helping farmers detect issues early and take preventive actions. The project focuses on:

- Optimizing training with custom data augmentation.
- Experimenting with various YOLO model sizes and configurations.
- Providing explainable predictions for better model interpretability.

## Dataset
The dataset contains images of various crop diseases, divided into categories like *Pepper Bacterial Spot*, *Corn Common Rust*, and others. Bounding boxes are provided for the diseased areas.

- **Training Data**: `/data/Train.csv`
- **Test Data**: `/data/Test.csv`
- **Sample Images**: Available in `/data/images/`


Running the Experiments
This project includes experiments with different configurations of YOLO. Notebooks are available in /notebooks for each configuration:

Experiment 1: Basic YOLO Training
Experiment 2: Data Augmentation with Albumentations
Experiment 3: Custom Training Loop
Custom Training Loop (Example)
To run a custom training loop, execute the following script:

bash
Copy code
python src/train_custom_loop.py
Results and Evaluation
The following table summarizes the performance across different model configurations.

Model	Image Size	Epochs	mAP	Inference Time
YOLOv8n	416	5	0.82	0.05s
YOLOv8s	540	10	0.88	0.07s
YOLOv8n (Custom Augmentation)	256	7	0.85	0.06s
Confusion Matrix and Model Performance

Observations

![image](https://github.com/user-attachments/assets/85e4baa0-8d62-4d54-b3c3-0f639d3db518)

Data Augmentation: Increased generalizability, especially on classes with fewer samples.
Custom Training Loop: Improved flexibility, allowing for fine-grained control over the training process.
Inference Time: YOLOv8 Nano model shows promise for real-time deployment on edge devices.
Future Work
Implement more sophisticated explainability techniques.
Experiment with YOLOv8’s larger models for even higher accuracy.
Explore model compression techniques for deployment on low-resource devices.
