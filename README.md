# cifar10-ann-cnn-cnnwithaugmentation
Comparative study of ANN and CNN on CIFAR-10 image classification, including CNN performance with and without data augmentation using Keras.


## Project Description
This project explores and compares the performance of **Artificial Neural Networks (ANN)** and **Convolutional Neural Networks (CNN)** on the **CIFAR-10 image classification dataset**.  
Additionally, the effect of **data augmentation** on CNN performance is analyzed to improve generalization and reduce overfitting.  

The project is implemented using **Colab python and Keras**, and demonstrates key concepts in deep learning such as model evaluation, confusion matrix analysis, and augmentation techniques.

---

## Dataset
- **Dataset:** CIFAR-10  
- **Number of classes:** 10 (airplane, automobile, bird, cat, deer, dog, frog, horse, ship, truck)  
- **Training samples:** 50,000  
- **Test samples:** 10,000  
- Images are **32x32 RGB**.

---

## Models Implemented

### 1. ANN (Artificial Neural Network)
- Fully connected layers
- Input flattened from 32x32x3
- **Training epochs:** 5
- Compared baseline accuracy with CNN

### 2. CNN (Convolutional Neural Network)
- Two convolutional layers with ReLU activation and max pooling
- Fully connected layers at the end
- **Training epochs:** 10
- Evaluated **without data augmentation**

### 3. CNN + Data Augmentation
- Applied augmentation techniques during training:
  - Rotation (`rotation_range=15`)
  - Width & height shifts (`0.1`)
  - Horizontal flip
  - Zoom (`0.1`)
  - **Training epochs**: 20
- Trained a fresh CNN on augmented data to evaluate improvement

---

## Results

| Model | Test Accuracy |
|-------|---------------|
| ANN | 49% |
| CNN (without augmentation) | 70% |
| CNN (with augmentation) | 75% |

**Observations:**
- CNN outperforms ANN significantly due to convolutional feature extraction.
- Data augmentation improves CNN accuracy by reducing overfitting and enhancing generalization.
- Confusion matrix analysis shows that visually similar classes (like cats and dogs) are better classified with augmentation.

---

## Confusion Matrix

- Confusion matrices were generated for ANN and CNN **with and without augmentation** to analyze class-wise performance.
- Example insight: The CNN with augmentation correctly classifies more images in classes that were previously confused.

*(Optional: Include images/plots of confusion matrix here if saved in `images/` folder)*

---

## How to Run

1. Clone the repository:
   ```bash
   git clone https://github.com/samia0101/cifar10-ann-cnn-cnnwithaugmentation.git

