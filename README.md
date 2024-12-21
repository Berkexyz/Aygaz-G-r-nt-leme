# 🐾 Aygaz Görüntü İşleme Kampı 🔍

## 📌 Projenin Amacı ve Kapsamı
Bu proje, görüntü işleme ve derin öğrenme tekniklerini kullanarak **10 farklı hayvan türünü sınıflandırmaya yönelik bir yapay zeka modeli geliştirmeyi** amaçlamaktadır. 

### 🔍 Sınıflandırılan Hayvan Türleri:
- Leopar 🐆
- Yunus 🐬
- Aslan 🦁
- Tilki 🦊
- Elk (Geyik) 🦌
- Tavşan 🐇
- At 🐎
- Sincap 🐿️
- Yarasa 🦇
- Goril 🦍

### 🔄 Kullanılan Teknikler:
- **Veri İşleme:** Görüntü manipülasyonları (ör. parlaklık artırma, renk sabitliği)
- **Veri Artırma:** Döndürme, kaydırma, zoom yapma gibi veri çeşitlendirme işlemleri
- **Derin Öğrenme:** CNN modeliyle sınıflandırma

---

## 🛠️ Kullanılan Kütüphaneler:
```python
import os
import numpy as np
import shutil
import random
import cv2
import matplotlib.pyplot as plt
from glob import glob
from sklearn.model_selection import train_test_split
from sklearn.preprocessing import LabelEncoder
from tensorflow.keras.preprocessing.image import ImageDataGenerator
from tensorflow.keras.models import Sequential
from tensorflow.keras.layers import Conv2D, MaxPooling2D, Flatten, Dense, Dropout, BatchNormalization
from tensorflow.keras.utils import to_categorical

📊 Veri Seti Hazırlığı
  1.Veri Seçimi: Her hayvan sınıfından 650 adet görsel.
  2.Veri Yapılandırması: Eğitim (%80) ve doğrulama (%20) olarak bölme.
  3.Veri Artırma: Görselleri manipüle ederek çeşitlilik sağlama.
  4.Etiketleme: Görselleri sınıflarına göre etiketleme.


🧠 Model Yapısı
  1.Katmanlar:
    -Conv2D: Görüntüden özellik çıkarımı
    -MaxPooling2D: Boyut azaltma
    -Flatten: Verileri düzleştirme
    -Dense: Tam bağlı katman
  2.Aktivasyon Fonksiyonları: relu ve softmax
  3.Optimizasyon: Adam
  4.Kayıp Fonksiyonu: categorical_crossentropy


🚀 Model Eğitimi ve Performansı
  -Batch Boyutu: 32
  -Epoch Sayısı: Belirlenmiş eğitim sürecine göre.
  -Başarı Kriteri: Doğruluk (accuracy)

📈 Sonuçların Görselleştirilmesi
Modelin başarısı, doğruluk ve kayıp grafikleriyle görselleştirilmiştir.





















