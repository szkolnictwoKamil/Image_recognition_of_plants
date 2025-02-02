# Image Recognition of Plants with Transfer Learning and Feature Compression

## **Project Overview**  
This project focuses on the **classification of plant species using deep learning models** while optimizing memory usage. The primary objective is to verify whether **compressed neural networks** can achieve classification accuracy comparable to standard, uncompressed architectures, while significantly reducing memory and computational requirements.  

To achieve this, the project explores **transfer learning**—leveraging pretrained models to improve training efficiency—and **feature dimensionality reduction** techniques such as **Principal Component Analysis (PCA)** and **Linear Discriminant Analysis (LDA)** to compress feature representations. By employing these techniques, the aim is to develop **lightweight, self-sufficient models** suitable for deployment in environments with limited computational resources, such as **mobile applications for plant recognition**.  

The effectiveness of these models is evaluated on two widely used plant image datasets:  
- **GRASP-125**, a dataset designed for mobile plant identification in Greek national parks.  
- **Oxford 102 Flower**, a standard benchmark dataset for flower classification.  

---

## **Repository Structure**  

- **`augmentation/`** – Jupyter Notebook implementing data augmentation techniques to improve model generalization.  
- **`data_encoding/`** – Notebook for encoding and preprocessing image features.  
- **`training/`** – Folder containing five trained models.  
- **`model_analysis/`** – Two notebooks analyzing model performance on the **GRASP-125** and **Oxford 102 Flower** datasets.  

---

## **Datasets**  

### **GRASP-125**  
- Contains **16,327 images** of vascular plants from **125 species**.  
- Originally developed for a **mobile application** designed for tourists and nature enthusiasts visiting **Greek national parks (Oiti & Parnassus)**.  

### **Oxford 102 Flower**  
- Comprises **8,189 images** across **102 flower species** commonly found in the **United Kingdom**.  
- Developed by the **University of Oxford** to support research in **image classification and computer vision**.  

---

## **Models and Techniques**  

To improve model efficiency and reduce memory usage, the following deep learning architectures were implemented:  

1. **MobileNetV2** – A lightweight convolutional neural network pretrained on ImageNet, serving as the baseline model.  
2. **SEResNet** – A Squeeze-and-Excitation ResNet variant that enhances feature extraction.  
3. **PCA+Dense** – A model using **Principal Component Analysis (PCA)** for dimensionality reduction, followed by fully connected layers.  
4. **PCA+SepConv** – Similar to PCA+Dense but utilizing **Separable Convolutions** for improved efficiency.  
5. **LDA+Dense** – A variation of PCA+Dense where **Linear Discriminant Analysis (LDA)** replaces PCA for feature compression.  
6. **LDA+SepConv** – A version of LDA+Dense that incorporates **Separable Convolutions**.  

These models employ **transfer learning**, leveraging pretrained weights to improve training efficiency while reducing the need for large labeled datasets. Feature reduction techniques such as **PCA and LDA** further optimize model performance by eliminating redundant information, leading to **smaller, more efficient models**.  The models can be found [HERE](https://drive.google.com/drive/folders/1VjjN_BTZ8f6CZ4vmJov4A2Gtj8vpJ6Cm?usp=sharing).

---

## **Results & Analysis**  

This study demonstrates that **memory-efficient neural networks** can achieve high classification accuracy while significantly reducing computational and memory requirements. Integrating **transfer learning** and **feature dimensionality reduction (PCA/LDA)**, allows to successfully develop **lightweight models** suitable for real-world applications, particularly in mobile plant recognition tools.  

The results highlight the potential of **compressed neural architectures** in image classification tasks, offering an effective alternative to traditional deep learning models that require **substantial memory and computational resources**.  
