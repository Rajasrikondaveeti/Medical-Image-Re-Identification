
# Multimodal Medical Image Augmentation and Classification

## 📁 Project Structure

This project is focused on medical image preprocessing using data augmentation techniques. It includes code for augmenting medical image datasets to improve model robustness and generalization.

```
.
├── all_model_code.ipynb
├── compa_multimodal_dataset2.zip
└── multimodal_dataset_medical_data.zip
```

## 📘 Description

### Notebook: `all_model_code.ipynb`
This Jupyter notebook contains code for:

- Loading and preprocessing a multimodal medical image dataset.
- Applying **image augmentation** using `ImageDataGenerator` from TensorFlow/Keras.
- Saving augmented images (500 per class) resized to 100x100 pixels.
- Organizing data into class-based folders.

Augmentation techniques used:
- `rotation_range=15`
- `zoom_range=0.1`
- `horizontal_flip=True`

The code dynamically handles folders for each class and saves augmented data into a separate output directory.

---

## 📊 Datasets

### 1. `compa_multimodal_dataset2.zip`
Contains multimodal medical image data organized into class-based folders.

### 2. `multimodal_dataset_medical_data.zip`
Another version of a multimodal dataset used for experimentation or training.

> **Note**: The dataset must be extracted and provided in the expected folder structure prior to running the notebook.

---

## 🛠️ Dependencies

- Python ≥ 3.8
- TensorFlow ≥ 2.x
- NumPy
- tqdm
- Keras (included in TensorFlow)

You can install dependencies with:

```bash
pip install tensorflow numpy tqdm
```

---

## 🐍 Python Version

The notebook expects Python 3.8+.
You can check your version using:

```bash
python --version
```

---

## ▶️ How to Use

1. Extract the dataset zips into appropriate folders.
2. Update dataset paths in the notebook if necessary.
3. Run `all_model_code.ipynb` step-by-step.
4. Augmented data will be saved into the output directory specified in the code.

---

## 📌 Output

- Augmented dataset saved under a directory named (e.g., `dataset2`).
- Each class contains 500 new images of size 100x100.

---

## 📩 Contact

For any questions or issues, please reach out to the project author.

