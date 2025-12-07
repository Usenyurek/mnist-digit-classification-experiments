# MNIST Digit Classification: ANN vs CNN 🔢

This project demonstrates a Deep Learning solution for the **Kaggle Digit Recognizer** competition. The goal is to correctly classify handwritten digits (0-9) using the famous MNIST dataset.

I implemented and compared two different Deep Learning architectures within a single notebook to demonstrate the significant performance improvement provided by **Convolutional Neural Networks (CNN)** over standard **Artificial Neural Networks (ANN)**.

## Project Overview
* **Dataset:** MNIST (via Kaggle)
* **Input:** 28x28 pixel grayscale images.
* **Goal:** Classify images into 10 classes (Digits 0-9).
* **Approach:** Comparative analysis of a Baseline Dense Model vs. a CNN Model.

## Results & Performance
I trained both models on the same training set and evaluated them on the Kaggle test set.

| Model Architecture | Method | Accuracy | Observation |
|---|---|---|---|
| **Model 1 (Baseline)** | Simple ANN (Dense Layers) | **97.30%** | Input was flattened (`784,`). Fast training but loses spatial relationships between pixels. |
| **Model 2 (Enhanced)** | **CNN (Convolutional)** | **98.72%** | Used `Conv2D` & `MaxPooling`. Significantly reduced the error rate by learning spatial hierarchies (shapes, edges). |

## Techniques & Technologies
* **Languages & Libraries:** Python, TensorFlow (Keras), Pandas, NumPy, Matplotlib.
* **Data Preprocessing:**
    * **Normalization:** Scaled pixel values from range [0, 255] to [0, 1] for faster convergence.
    * **Reshaping:** Reshaped flat data into `(28, 28, 1)` format for the CNN input.
* **Model Architectures:**
    * **ANN:** Uses `Flatten` followed by `Dense` layers with ReLU activation.
    * **CNN:** Uses a stack of `Conv2D` (Feature Extraction) and `MaxPooling2D` (Downsampling) layers before the final classification head.
* **Optimization:** Used **Adam** optimizer and **Sparse Categorical Crossentropy** loss function.

##


Bu projede el yazısı rakamları (0-9) sınıflandırmak için Derin Öğrenme (Deep Learning) modelleri geliştirdim.

# Sonuçlar
İki farklı mimariyi test ettim ve sonuçları karşılaştırdım:

| Model Mimarisi | Yöntem | Doğruluk (Accuracy) | Açıklama |
|---|---|---|---|
| **Model 1** | Simple ANN (Dense Layers) | %97.30 | Pikseller düzleştirilerek (Flatten) işlendi. |
| **Model 2** | **CNN (Convolutional)** | **%98.72** | Görüntü işleme filtreleri (Conv2D & MaxPooling) kullanıldı. |

# Öğrendiklerim
* **Veri İşleme:** Normalizasyon ve Reshape işlemleri (28x28x1).
* **Dense Network:** Temel yapay sinir ağı kurulumu.
* **CNN (Evrişimli Sinir Ağları):** Resimlerdeki desenleri ve şekilleri yakalamak için filtreleme yöntemleri.
* **Overfitting Önleme:** Dropout ve Pooling katmanlarının etkisi.
