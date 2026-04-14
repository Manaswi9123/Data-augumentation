# Data-augumentation
# 🔄 Robust Computer Vision: Data Augmentation in TensorFlow

A common problem in Deep Learning is having a small dataset, which leads to a model that "memorizes" training samples rather than learning general patterns. This repository demonstrates how to use **Data Augmentation** to create variations of images, effectively teaching the model to recognize objects regardless of their orientation, size, or lighting.

---

## 🛠️ The Tech Stack
* **Language:** Python
* **Deep Learning Framework:** TensorFlow & Keras
* **Image Processing:** OpenCV (cv2), PIL
* **Visualization:** Matplotlib, NumPy
* **Dataset:** Flower Photos (Sunflowers, Daisy, Dandelion, Roses, Tulips)

---

## 🧠 Key Concepts Implemented

### 1. The Overfitting Baseline
* Built a standard **Convolutional Neural Network (CNN)** without augmentation.
* **Observation:** The model achieved high training accuracy but poor validation accuracy, indicating it was unable to generalize to new, unseen images of flowers.

### 2. Data Augmentation Layers
Integrated a preprocessing "Augmentation Pipeline" directly into the Keras model. Techniques used include:
* **Random Flip:** Flipping images horizontally and vertically.
* **Random Rotation:** Rotating images by a certain factor to handle different camera angles.
* **Random Zoom:** Zooming in and out to make the model scale-invariant.
* **Contrast/Brightness:** Adjusting image properties to handle different lighting conditions.



### 3. Improved CNN Architecture
Implemented a robust Sequential model:
* **Preprocessing:** `layers.Rescaling` to normalize pixel values.
* **Augmentation:** Applied the transformation layers described above.
* **Extraction:** Multiple `Conv2D` and `MaxPooling2D` layers to capture spatial features.
* **Regularization:** Included **Dropout** layers to further prevent overfitting.

---

## 📊 Results & Impact
* **Generalization:** By using augmentation, the "gap" between training and validation accuracy was significantly reduced.
* **Robustness:** The model became capable of identifying a "Sunflower" even if it was upside down, zoomed in, or partially rotated.



---

## 🚀 How to Run

1. **Clone the repository:**
   ```bash
   git clone [https://github.com/Manaswi9123/Python-DataScience-Fundamentals.git](https://github.com/Manaswi9123/Python-DataScience-Fundamentals.git)

2. **Install Dependencies:**
      pip install tensorflow opencv-python matplotlib pillow
   
3. **Execute:**
        Open DataAugmentation.ipynb in Jupyter or VS Code. The notebook will automatically download the flowers dataset and            begin the training process.
