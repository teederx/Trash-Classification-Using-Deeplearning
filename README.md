# ♻️ Trash Classification using Deep Learning (PyTorch)

![PyTorch](https://img.shields.io/badge/PyTorch-Deep%20Learning-red?logo=pytorch)
![Python](https://img.shields.io/badge/Python-3.x-blue?logo=python)
![Dataset](https://img.shields.io/badge/Dataset-TrashNet-orange)
![Status](https://img.shields.io/badge/Project-Completed-brightgreen)
![License](https://img.shields.io/badge/License-MIT-green)

---

## 👨‍💻 Author

**Idowu Favour**  
Email: idowufavour07@gmail.com  

---

## 📌 Overview

This project uses a **Convolutional Neural Network (CNN)** built with PyTorch to classify images of trash into different categories using the TrashNet dataset.

It demonstrates how deep learning can be applied to environmental sustainability and automated waste classification systems.

---

## 🖼️ Sample Predictions

| Input Image | Prediction |
|-------------|------------|
| Image 1 | Plastic |
| Image 2 | Glass |
| Image 3 | Paper |

---

## 📊 Dataset

- Dataset: TrashNet
- Source: KaggleHub
- Type: Image classification dataset (folder structured)

### Download Dataset
```python
import kagglehub

path = kagglehub.dataset_download("feyzazkefe/trashnet")
```
---
## ⚙️ Data Preprocessing

The following transformations were applied:

Random horizontal flip
Random rotation (±15°)
Resize images to 64×64
Convert to tensor
Normalize (mean=0.5, std=0.5)
Dataset Split
80% Training
20% Testing

## 🧠 Model Architecture

A custom CNN model was built with:

Input → Conv → BN → ELU → MaxPool → Conv → BN → ELU → MaxPool → Conv → BN → ELU → MaxPool → Conv → BN → ELU → AdaptiveAvgPool → Fully Connected Layers → Output

## 🚀 Training Setup
Parameter	Value
Loss Function	CrossEntropyLoss
Optimizer	Adam
Learning Rate	0.001
Scheduler	StepLR
Epochs	50
Device	GPU (if available)

## 📈 Training Process
Epoch 1  | Loss: ...
Epoch 10 | Loss: ...
Epoch 50 | Loss: ...

## 🧪 Evaluation

Model evaluation includes:

Test Loss
Test Accuracy

Performed using torch.no_grad() for efficiency.

## 💾 Save Model
model.pth

## 🔍 Inference

To predict a new image:

output = net(img)
_, prediction = torch.max(output, 1)
print(dataset.classes[prediction.item()])

## 📁 Project Structure
Trash-Classification/
│
├── notebook.ipynb
├── model.pth
├── new_images/
└── README.md

## 🛠️ Installation
pip install torch torchvision pillow kagglehub

## ▶️ How to Run
Clone repository
Install dependencies
Run notebook step-by-step
Train model
Test predictions

## 🌱 Future Improvements
Increase image size (64 → 128/224)
Use pretrained models (ResNet, EfficientNet)
Deploy using Streamlit or Flask
Add real-time camera prediction

## 📜 License
MIT License

## 📬 Contact
Idowu Favour
Email: idowufavour07@gmail.com
