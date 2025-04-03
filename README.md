# 🧠 Brain Tumor Segmentation with UNet-VGG16

## 📌 Introduction  
Brain tumor segmentation in magnetic resonance imaging (MRI) plays a crucial role in medical diagnostics and treatment planning. However, accurate and automated segmentation remains a challenging task due to the complex nature of tumor morphology and variations in imaging conditions. This repository presents an implementation of a deep learning-based segmentation model, leveraging the UNet architecture with a VGG16 encoder for feature extraction. The model benefits from transfer learning, utilizing the pre-trained VGG16 network to enhance feature representation while maintaining the spatial resolution necessary for precise segmentation. Inspired by the study *"UNet-VGG16 with transfer learning for MRI-based brain tumor segmentation"* by Anindya Apriliyanti Pravitasari et al., this implementation aims to achieve high accuracy in delineating tumor regions from MRI scans. The model is trained on the LGG Segmentation Dataset and optimized using Binary Cross Entropy loss with Adam optimization. This work contributes to advancing automated medical image segmentation, potentially aiding clinicians in faster and more reliable tumor diagnosis.  

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

![Dataset Sample](/Images/dataset.png)

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

![Loss Curve](/Images/plot.png)

## 🎯 Results
After training, the model's performance is evaluated by comparing predicted masks with ground truth masks. Below are some sample predictions:

![Sample Predictions](/Images/pred.png)

## 📜 License
This project is licensed under the **GNU Affero General Public License v3.0**.

## 📬 Get in Touch
For any inquiries or collaborations, feel free to contact me!

- 📧 [ali0aliakbari0@gmail.com](mailto:ali0aliakbari0@gmail.com)
- 🔗 [LinkedIn](http://linkedin.com/in/ali-aliakbari-602227167)  

Let's connect and discuss more! 🚀

