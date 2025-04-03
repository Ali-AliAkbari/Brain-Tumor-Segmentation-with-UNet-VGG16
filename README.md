# 🧠 Brain Tumor Segmentation with UNet-VGG16

## 📌 Introduction
This repository presents an implementation of a brain tumor segmentation model using a UNet architecture with a VGG16 backbone for feature extraction. The approach is inspired by the paper:

**"UNet-VGG16 with transfer learning for MRI-based brain tumor segmentation"**
by Anindya Apriliyanti Pravitasari et al.

The model is designed to segment MRI brain scans, identifying tumor regions with high accuracy.

## 📂 Dataset
The dataset used for this project is the **LGG Segmentation Dataset**, available on Kaggle. It contains MRI scans along with their corresponding tumor masks. The dataset structure is as follows:

```
/kaggle/input/lgg-mri-segmentation/kaggle_3m
│── Patient_001
│   │── Image.tif
│   │── Image_mask.tif
│── Patient_002
│── ...
```

A sample of the dataset is visualized below:

![Dataset Sample](sample_dataset.png)

## 🏗️ Model Architecture
The implemented model is based on the UNet architecture with a **VGG16** feature extractor. The core components are:

- **VGG16 Backbone**: Extracts hierarchical spatial features from input images.
- **Double Convolution Blocks**: Applied at each level of the encoder and decoder to refine feature representations.
- **Upsampling Layers**: Restore the spatial resolution of the segmented regions.
- **Skip Connections**: Enable detailed features from the encoder to be preserved in the decoder.
- **Final Convolution Layer**: Produces the segmentation mask as the output.

## 📚 Training Process
The model is trained using the **Binary Cross Entropy (BCE) Loss with Logits** and optimized using **Adam**. Training details:

- **Dataset split**: 80% training, 20% validation.
- **Batch size**: 16
- **Learning rate**: 4e-4
- **Epochs**: 30

The training and validation loss curves are shown below:

![Loss Curve](loss_plot.png)

## 🎯 Results
After training, the model's performance is evaluated by comparing predicted masks with ground truth masks. Below are some sample predictions:

![Sample Predictions](sample_predictions.png)

## 📜 License
This project is licensed under the **GNU Affero General Public License v3.0**.

## 📬 Get in Touch
For any inquiries or collaborations, feel free to contact me!

- 📧 Email: [Your Email]
- 🔗 LinkedIn: [Your LinkedIn Profile]
- 🐦 Twitter: [Your Twitter Handle]

Let's connect and discuss more! 🚀

