# ⚡ Photovoltaic Panel Fault Classification using Transfer Learning

This project presents a deep learning-based approach to automatically **identify and classify faults in solar (photovoltaic) panels** using RGB image data taken from [kaggle](https://www.kaggle.com/datasets/pythonafroz/solar-panel-images/data). The model leverages **transfer learning with a pretrained ResNet-18** architecture to classify panel conditions into one of six categories.

---

## 📁 Dataset

The dataset is organized into folders corresponding to each fault type: Bird drop, clean, Dusty, Electrical damage, Physical damage, Snow Covered

Each folder contains `.jpg` images of photovoltaic panels exhibiting that specific condition.

---

## 🧠 Model Overview

- **Architecture**: ResNet-18 (pretrained on ImageNet)
- **Approach**: Fine-tune the final layer to classify images into 6 custom classes
- **Input**: RGB images resized and normalized to ImageNet standards

---

## 🛠️ Tools & Libraries

- PyTorch
- Torchvision
- scikit-learn
- Matplotlib
- PIL (Pillow)

---

## 🧪 Training and Evaluation

- Dataset is split into **training** and **validation** sets
- Basic preprocessing: Resize, CenterCrop, Normalize
- Optimizer: Adam
- Loss: CrossEntropyLoss

After training, the model achieved approximately **73% accuracy** on the validation set.

---

## 🚀 How to Run

- Clone the repo and get the original dataset from [kaggle](https://www.kaggle.com/datasets/pythonafroz/solar-panel-images/data) for the complete dataset if you want to train
  ```git clone https://github.com/vdhkcheems/EAD-assignment.git```
- setup a python env and set as source according to your OS
- install requirements accordingly whether you want to edit training or just test inference.
  ```pip install - r requirements-training.txt```
  or
  ```pip install - r requirements-inference.txt```
- For inference put your desired image in the 'new' directory under the name 'img.jpg' and then run the inference,ipynb file. Last cell will give the predicted label
