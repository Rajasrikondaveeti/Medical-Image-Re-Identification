
# Medical Image Re-identification Using Modality-Aware Deep Learning
## Project Summary
Project Summary: Medical Image Re-identification Using Modality-Aware Deep Learning

Medical image re-identification is an important task in healthcare systems, as medical images from different modalities such as X-ray, MRI, CT, and dermoscopic imaging exhibit distinct visual characteristics. Applying a single deep learning model to all modalities often leads to reduced performance. This project proposes a modality-aware medical image re-identification framework that accurately identifies the imaging modality of an input image and processes it using an appropriate deep learning model.

The proposed pipeline begins with image preprocessing using CLAHE (Contrast Limited Adaptive Histogram Equalization). CLAHE enhances local contrast and improves the visibility of important anatomical and pathological details while limiting noise amplification. This preprocessing step ensures that the input images are of improved quality and are better suited for deep feature extraction.

Following preprocessing, the enhanced images are passed to a Comparator-based Modality Prediction Algorithm (COMPA), which is responsible for identifying the imaging modality of each medical image. COMPA analyzes visual patterns and intensity characteristics to determine whether the image belongs to a specific modality. Accurate modality identification enables the system to route images to the most suitable classification model.

Once the modality is identified, the image is forwarded to a modality-specific Convolutional Neural Network (CNN). In this project, MobileNet is used as the core CNN architecture due to its lightweight design, reduced computational complexity, and high efficiency. MobileNet employs depthwise separable convolutions, which significantly decrease the number of parameters while maintaining strong feature representation capabilities. This makes it well-suited for medical imaging applications, especially in resource-constrained environments.

To improve model generalization and reduce overfitting, data augmentation techniques are applied during training. These include transformations such as rotation, flipping, scaling, and brightness adjustment. Data augmentation artificially increases dataset diversity and helps the model become more robust to variations in image acquisition and orientation.

Overall, the proposed system integrates CLAHE-based preprocessing, COMPA-driven modality identification, and MobileNet-based CNN classification, supported by data augmentation, to create an efficient and accurate medical image re-identification framework. The approach enhances classification performance while maintaining computational efficiency, making it suitable for real-world clinical and research applications.

## 📁 Project Structure

This project is focused on medical image preprocessing using data augmentation techniques. It includes code for augmenting medical image datasets to improve model robustness and generalization. It also includes applying the modality speific CNN model and retrieving the patient id.

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

