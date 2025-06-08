# 👁 Retinopathy Severity Classification

## 🏆 Overview

This project classifies the severity of retinopathy from retinal fundus images into three categories:

* **Mild**
* **Moderate**
* **Severe**

The goal is to support ophthalmologists by enabling faster and more accurate screening through machine learning and deep learning models.

---

## 📂 Dataset Summary

| Class    | Image Count | Avg Width | Avg Height | Mean Pixel | Std Dev Pixel |
| -------- | ----------- | --------- | ---------- | ---------- | ------------- |
| Mild     | 811         | 816.92 px | 773.65 px  | 73.69      | 39.72         |
| Moderate | 569         | 823.19 px | 643.67 px  | 76.73      | 31.92         |
| Severe   | 384         | 815.62 px | 638.03 px  | 76.42      | 32.27         |

* **Mean pixel values** around 73-77 suggest moderately dark images.
* **Image sizes** vary slightly but are resized during preprocessing.

---

## ⚠️ Class Imbalance

| Class    | Weight | Interpretation                      |
| -------- | ------ | ----------------------------------- |
| Mild     | 0.7247 | Over-represented (more samples)     |
| Moderate | 1.0332 | Roughly balanced                    |
| Severe   | 1.5333 | Under-represented (needs attention) |

To handle this, **class weights** were used during model training.

---

## 📊 Model Comparison

| Model                  | Accuracy | F1 Score | Test Loss |
| ---------------------- | -------- | -------- | --------- |
| CNN (Baseline)         | 0.72     | 0.64     | 0.57      |
| DenseNet121            | 0.87     | 0.87     | 0.83      |
| DenseNet201            | 0.87     | 0.87     | 0.95      |
| MobileNetV2            | 0.76     | 0.74     | 0.57      |
| **Ensemble (121+201)** | **0.88** | **0.88** | **0.25**  |

---

## 📊 Final Recommendation

### ✨ Deploy the **Ensemble Model (DenseNet121 + DenseNet201)**:

* Highest accuracy (**0.8868**) and F1 score (**0.8840**)
* Lowest test loss (**0.2510**)
* Ensures reliable and consistent performance in retinal disease detection

### ⚡ Ensure Real-time Inference:

* Optimize using **TensorFlow Lite** or **ONNX**
* Supports fast deployment in clinical or mobile environments

### 💼 Integrate with Diagnostic Systems:

* Embed model into hospital software or telemedicine apps
* Aids in reducing turnaround time for diagnosis

### ⚖️ Support Clinical Decision-making:

* Acts as a decision support tool
* Useful in remote areas with limited specialist access

### 🚀 Enable Scalable Screening:

* Deploy in primary health centers, mobile eye clinics
* Addresses specialist shortage and enables **early-stage detection**

---

## 🛠️ Tools & Technologies

* Python, TensorFlow, Keras
* DenseNet, MobileNet, CNNs
* Matplotlib, OpenCV

---

## 📚 License

This project is open-source under the MIT License.

---

## 📈 Future Work

* Add explainable AI (Grad-CAM)
* Build web-based interface for patient/doctor use
* Train on higher-resolution images for better precision

---

## 📅 Project Maintainer

**Manoj Kanna T.**
[LinkedIn](https://www.linkedin.com/in/manojkanna3690/)
Email: [manojthomas3690@gmail.com](mailto:manojthomas3690@gmail.com)
