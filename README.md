# Image-Forgery-Detection-using-CNN-and-Semantic-Segmentation

## 📌 Project Overview

This project addresses the rising issue of digital image forgery, which has severe implications in fields like journalism, legal evidence, and national security. It utilizes **Convolutional Neural Networks (CNN)** and **Semantic Segmentation** to detect and localize tampered regions in images at the pixel level.

The system integrates a pretrained deep learning model into a **Django-based web application**, offering a user-friendly interface for real-time image forgery detection.

---

## 👨‍💻 Team Members

* P Vidhath – 4SF22CS128
* Sushrutha Shanbhogue – 4SF22CS225
* Raghavendra SS – 4SF22CS158
* Venkatesh – 4SF22CS243

**Guided by**: Mr. Srinivas PM, Assistant Professor, Department of CSE, SCEM

---

## 🎯 Objectives

* Detect and localize image forgeries such as **copy-move** and **splicing**.
* Achieve **pixel-level localization** of tampered areas using Semantic Segmentation.
* Ensure the system is **scalable** and **accessible** to non-technical users via a web application.
* Handle challenges like **compression artifacts**, **noise**, and **scaling**.

---

## 🛠️ Technology Stack

* **Machine Learning:** CNNs, UNet, DeepLabV3 (PyTorch/TensorFlow)
* **Web Framework:** Django (Python)
* **Frontend:** HTML, CSS, JavaScript
* **Image Analysis:** Error Level Analysis (ELA)

---

## 🔍 Features

* Upload an image and detect forged regions using a CNN-based model.
* Pixel-level mask visualization of tampered areas.
* Real-time ELA visualization.
* Web-based interface for ease of access.

---

## 🧠 Methodology

### Model Development

* **Dataset Used**: CASIA v2, CoMoFoD, or custom datasets
* **Preprocessing**: Resizing, normalization, pixel-level masks
* **Architecture**: Pretrained CNN backbone (e.g., ResNet, EfficientNet) + segmentation head (UNet/DeepLabV3)
* **Training**: Loss functions like cross-entropy, metrics like IoU, Dice Coefficient

### Error Level Analysis (ELA)

* Highlights inconsistencies in compression to detect tampering visually.
* Used alongside the deep learning model for verification.

### Web Implementation

* **Backend**: Django project handles uploads, inference, and result rendering.
* **Frontend**: User interface for uploading images and viewing output masks.

---

## 🚀 How to Run

1. **Clone the repository**
2. Set up a virtual environment and install dependencies.
3. Load the pretrained model (`.pt` or `.h5` format).
4. Run the Django development server:

   ```bash
   python manage.py runserver
   ```
5. Access the web interface at `http://127.0.0.1:8000/`.

---

## 📊 Results

* High accuracy on common forgery types (copy-move, splicing)
* Robust performance under compression and noise
* Slight drop in performance for complex forgeries like deepfakes

### Performance Metrics

* Pixel Accuracy
* IoU (Intersection over Union)
* Dice Coefficient
* Confusion Matrix (included in report)

---

## ✅ Strengths

* **Accurate** pixel-level tampering localization
* **Lightweight** and **scalable** web application
* **User-friendly interface** for technical and non-technical users

---

## ⚠️ Limitations

* Lower performance on deepfake detection
* GPU dependency for real-time inference
* Limited training on emerging forgery types

---

## 🔮 Future Work

* Integration of **Vision Transformers** and **GAN-based models**
* **Deepfake detection** using temporal CNNs
* Deployment on **edge devices** like smartphones
* Adding **batch processing** and **forensic report generation**

---

## 📚 References

The project is backed by a comprehensive literature survey of 30+ academic papers ranging from CNN architectures, semantic segmentation techniques, GANs, hybrid models, and dataset enhancements. Please refer to the full [Mini Project Report](./Mini-Project%20Report.pdf) for complete citations.
