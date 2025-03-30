## **COMPI Project**  
**Team:** Mohammed Dahbani & Mahmoud Mokrane  

---

### **Project Overview**  
This project implements an **Optimal Transport (OT)-based pipeline** for image processing, focusing on **image restoration**. The workflow consists of an **offline training phase** and an **inference phase** for testing.

The project is structured around two main Jupyter notebooks:
- **`DOT.ipynb`**: Implements the OT pipeline and testing phase.
- **`Dataset.ipynb`**: Prepares the dataset used for training and testing.

---

### **Dataset Preparation**  
The dataset consists of images categorized into different folders for training and testing:

#### **Training Data (Offline Phase Input)**  
Organized into **six folders**, containing :
- **10 clean images** (original high-quality images) (2 folders)
- **10 noisy images** (Gaussian noise applied) (2 folders)
- **10 restored images** (Gaussian blur applied for denoising) (2 folders)

#### **Testing Data (Inference Phase Input)**  
Organized into **three separate folders**:
- **Clean test image**
- **Noisy test image**
- **Restored test image**


---

### **DOT Pipeline**  
The DOT (Deep Optimal Transport) pipeline consists of two main phases:

#### **1- Training Phase (Offline Phase)**  
1. **Encode Images**: Extracts feature representations from images.
2. **Compute the OT Operator**: Learns the optimal transport mapping between noisy and clean images.
3. **Apply the OT Transformer**: Transforms new images based on the learned mapping.

#### **2- Inference Phase (Testing Phase)**  
- Utilizes the pre-trained model to perform **predictions on new images**.
- Evaluates the quality of restoration on clean, noisy, and restored test images.

---

### **Testing Approach**  
We evaluate the pipeline using a **pre-trained Variational Autoencoder (VAE)**, following a reference research paper. The testing includes:
- **Paired image testing**: Using corresponding noisy and clean images.
- **Unpaired image testing**: Testing on unseen images to evaluate generalization.

---




