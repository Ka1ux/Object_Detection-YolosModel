# 🧠 Object Detection with YOLOS

A compact project that uses a pre-trained **YOLOS transformer model** to detect and label multiple objects in an image (clothes, accessories, people, etc.).  
Built using **PyTorch**, **Transformers (Hugging Face)**, and **Pillow**.

---

## 📸 Overview

This project uses the model `valentinafeve/yolos-fashionpedia` from Hugging Face to detect **fashion-related and general objects** in images.  
It returns bounding boxes with **labels and confidence scores** drawn over the image.

---

## 🚀 Features

- Detects multiple objects in one image  
- Uses transformer-based vision (**YOLOS**)  
- Draws bounding boxes and labels automatically  
- Easy to tweak detection thresholds and inputs  

---

## 🧰 Tech Stack

| Category | Tools |
|-----------|--------|
| **Language** | Python 3 |
| **Framework** | PyTorch |
| **Model** | Hugging Face Transformers (YOLOS) |
| **Imaging** | Pillow |
| **Plotting** | Matplotlib |
| **HTTP** | Requests |

---

## 💻 Installation

Run the commands below in Google Colab or your terminal.  
If using Colab, don’t forget to include `!` before each `pip install`.

```
# PyTorch (CUDA 12.1 variant for Colab)
!pip install torch==2.3.1+cu121 torchvision==0.18.1+cu121 torchaudio==2.3.1+cu121 --index-url https://download.pytorch.org/whl/cu121

# Transformers + utilities
!pip install transformers==4.41.2

# Image processing and display
!pip install pillow matplotlib requests

# Fix NumPy if binary incompatibility occurs
!pip install numpy==1.26.4

```
## 🖼️ Example Output

The image will appear with red bounding boxes and confidence labels, for example:
```
Person (0.98)
Hat (0.92)
Bag (0.87)
```
## Customization

You can adjust the confidence threshold in this line:
```
results = processor.post_process_object_detection(outputs, target_sizes=target_sizes, threshold=0.7)[0]
```
Try lowering to 0.5 to see more detections or increasing to 0.9 for higher accuracy.
