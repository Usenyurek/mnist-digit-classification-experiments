# MNIST Digit Classification Project 

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
