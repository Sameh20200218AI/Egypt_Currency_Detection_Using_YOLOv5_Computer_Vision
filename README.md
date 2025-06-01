# 🏦 Egyptian Currency Detection using YOLOv5

This project focuses on detecting and classifying Egyptian currency notes using a fine-tuned YOLOv5 object detection model. It leverages a labeled image dataset with 12 classes representing different denominations and sides (front/back) of Egyptian banknotes.

---

## 📌 Project Overview

- **Goal**: Detect and identify Egyptian banknotes in images using object detection.
- **Model**: YOLOv5 (fine-tuned).
- **Dataset**: 10,021 labeled images from Roboflow (resized to 640x640), annotated in YOLO format.
- **Classes**: 12 distinct classes representing the front and back sides of 5, 10, 20, 50, 100, and 200-pound notes.

---

## 🗂️ Dataset Details

- **Total Images**: 10,021  
  - **Training Set**: 8,016 images  
  - **Validation Set**: 2,005 images  
- **Image Size**: `640x640x3`
- **Format**: YOLO format (images + `.txt` annotations)

### 🏷️ Class Names:
| Class ID | Description               |
|----------|---------------------------|
| 0        | front of 10 pounds paper  |
| 1        | back of 5 pounds paper    |
| 2        | back of 50 pounds paper   |
| 3        | back of 10 pounds paper   |
| 4        | front of 100 pounds paper |
| 5        | back of 20 pounds paper   |
| 6        | front of 200 pounds paper |
| 7        | back of 200 pounds paper  |
| 8        | front of 50 pounds paper  |
| 9        | front of 20 pounds paper  |
| 10       | front of 5 pounds paper   |
| 11       | back of 100 pounds paper  |

---

## 🔧 Project Pipeline

1. **Library Imports**:  
   `os`, `cv2`, `numpy`, `matplotlib`, `sklearn`, `glob`, `IPython.display`

2. **Data Preparation**:
   - Dataset loaded from a `.zip` file
   - Extracted and organized with corresponding `.txt` annotations

3. **Visualization**:
   - Displayed 5 random samples from each of the 12 classes for inspection (total of 60 images)

4. **Model Loading**:
   - Loaded YOLOv5 pre-trained model via PyTorch Hub or official YOLOv5 repo

5. **Training**:
   - Epochs: `40`
   - Batch size: `32`
   - Fine-tuned on the custom Egyptian currency dataset

6. **Evaluation**:
   - Precision: `0.998`
   - Recall: `0.995`
   - mAP@0.5: `0.995`
   - mAP@0.5:0.95: `0.983`

7. **Testing**:
   - Performed detection on multiple unseen images
   - Output predictions with bounding boxes and confidence scores

8. **Model Saving**:
   - Trained model was saved for future inference use

---

## 🖼️ Results
![F1_curve(1).png](https://github.com/Sameh20200218AI/Egypt_Currency_Detection_Using_YOLOv5_Computer_Vision/blob/main/F1_curve%20(1).png)
![Sample Detection](assets/sample_detection.png)
![Sample Detection](assets/sample_detection.png)
![Sample Detection](assets/sample_detection.png)
![Sample Detection](assets/sample_detection.png)
