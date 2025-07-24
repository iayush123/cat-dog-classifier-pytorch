# 🐶😺 Cat vs Dog Image Classifier using PyTorch

This project is a **binary image classifier** that distinguishes between **cats and dogs** using **ResNet18** architecture and the **popular Cat-Dog dataset** from Kaggle.
---

## 📂 Dataset Used

- **Source**: [Kaggle - Cat and Dog Classification Dataset](https://www.kaggle.com/datasets/tongpython/cat-and-dog)
- **Structure**:
  - `/training_set/cats`
  - `/training_set/dogs`
  - `/test_set/cats`
  - `/test_set/dogs`

Images are resized and transformed using PyTorch `transforms`.

---

## 🧠 Model Architecture

We use **Transfer Learning** with pretrained **ResNet-18**, and fine-tune the final fully connected layer for 2-class output (cat/dog).

### 🔧 Architecture Highlights:
- `ResNet18` pretrained on ImageNet
- Final `fc` layer replaced with `nn.Linear(512, 1)` (for binary classification)
- `BCEWithLogitsLoss()` used as the loss function

---

## ⚙️ Training Details

| Parameter        | Value              |
|------------------|--------------------|
| Optimizer        | Adam               |
| Loss Function    | CrossEntropyLoss  |
| Epochs           | 20                 |
| Batch Size       | 32                 |
| Image Size       | 224x224            |
| Validation Split | 20% of training set|

---

## 📈 Results

| Metric      | Value     |
|-------------|-----------|
| **Best Accuracy (Val)** | ~94%       |
| **Final Test Accuracy** | ~93%       |
| **Loss Trend** | Training loss steadily decreased |

---

## 🚀 How to Run

1. Clone the repository:

```bash
git clone https://github.com/yourusername/cat-dog-classifier.git
cd cat-dog-classifier
