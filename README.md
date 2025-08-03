# DenseNet121-for-disaster-localization

This project leverages a **pretrained DenseNet121 architecture** for classifying aerial images into disaster-related categories using the AIDER dataset. The goal is to explore transfer learning in the context of emergency response systems powered by computer vision.

---

## Dataset: AIDER

- **Total Images:** 6,433 labeled aerial images  
- **Classes:** 5 emergency-related categories  
- **Split:**
  - **Training:** 5,469 images
  - **Validation:** 964 images

---

## Training Configuration

| Setting           | Value                            |
|------------------|----------------------------------|
| Optimizer        | Adam                             |
| Loss Function    | Sparse Categorical Crossentropy  |
| Epochs           | 30                               |
| Batch Size       | 64                               |
| EarlyStopping    | Patience = 5, Monitor = `val_loss` |
| Data Augmentation| Flip, Rotation, Translation, Contrast |
| Normalization    | Rescaling pixel values to `[0, 1]` |

---

## Performance Summary

| Metric                     | Value         |
|----------------------------|---------------|
| Best Training Accuracy   | **93.24%** (Epoch 12) |
| Best Validation Accuracy | **93.36%** (Epochs 9 & 12) |
| Best Validation Loss     | **0.2406** (Epoch 7) |
| Best Epoch               | Epoch 12 (EarlyStopping trigger)

> The model reached **93.36% validation accuracy** and **0.2406 validation loss**, demonstrating very strong performance for aerial disaster classification.

