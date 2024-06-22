# Fashion-mnist-classification

Bu proje, Aygaz Yapay Zekaya Giriş kursu kapsamında, Fashion MNIST veri setini kullanarak gri tonlamalı görüntüleri 10 kategoriye ayırmak için bir derin öğrenme modeli oluşturmayı ve değerlendirmeyi amaçlar. Doğruluk, F1 skoru, geri çağırma ve kesinlik metrikleri ile model performansı ölçülmüştür.

## Projenin Amacı

Bu projenin amacı, Fashion MNIST veri setini kullanarak derin öğrenme modelleriyle görüntü sınıflandırma yapmaktır. Bu sayede, görüntü işleme ve yapay zeka konularında temel bilgilerin pekiştirilmesi hedeflenmiştir.

## Kullanılan Veri Setleri

- **Fashion MNIST**: 28x28 boyutlarında 70,000 gri tonlamalı görüntü içeren bir veri setidir. Bu veri seti, 10 farklı kategoriye (T-shirt/top, Trouser, Pullover, Dress, Coat, Sandal, Shirt, Sneaker, Bag, Ankle boot) ayrılmıştır ve her kategori için 7,000 görüntü bulunmaktadır.

## Temel Bulgular

- **Doğruluk (Accuracy):** 
  - Eğitim setinde: 0.8554 
  - Test setinde: 0.7892
- **F1 Skoru:** 
  - Eğitim setinde: 0.8546 
  - Test setinde: 0.7899
- **Geri Çağırma (Recall):** 
  - Eğitim setinde: 0.8554 
  - Test setinde: 0.7892
- **Kesinlik (Precision):** 
  - Eğitim setinde: 0.8578 
  - Test setinde: 0.7999
- **Karmaşıklık Matrisi:** Modelin tahminlerinin doğruluğunu ve hatalarını sınıflandırmalar arasında göstermektedir.

## Gelecekteki Geliştirme Önerileri

1. **Model İyileştirme:**
   - Daha karmaşık modeller (örneğin, ResNet, Inception gibi) kullanarak doğruluğun artırılması.
   - Veri artırma (Data Augmentation) teknikleri kullanarak eğitim veri setinin genişletilmesi.
   - Düzenlileştirme (Regularization) teknikleri kullanarak modelin aşırı öğrenmesinin (overfitting) önlenmesi.

2. **Veri Ön İşleme İyileştirmeleri:**
   - Verilerin daha iyi normalize edilmesi.
   - Verideki gürültünün azaltılması.

3. **Hiperparametre Optimizasyonu:**
   - Grid Search veya Random Search yöntemleriyle en iyi hiperparametrelerin bulunması.
   - Bayesian Optimization gibi sofistike yöntemler kullanılarak hiperparametre aramasının yapılması.

4. **Daha Fazla Veri Toplama:**
   - Ek veri setlerinin kullanılması.
   - Farklı kaynaklardan veri toplanarak veri çeşitliliğinin artırılması.

## Teknik Detaylar:

1. Veri Seti: Fashion MNIST veri seti, 28x28 boyutunda gri tonlamalı 70,000 görüntü içerir. Toplamda 10 farklı kategori bulunmaktadır.

2. Model Oluşturma:
   - Derin öğrenme modeli Sequential API kullanılarak oluşturulmuştur.
   - Giriş katmanı olarak 28x28 boyutundaki görüntüler düzleştirilmiştir.
   - İki tam bağlantılı gizli katman eklenmiştir (128 ve 64 nöronlu).
   - Çıkış katmanı olarak 10 sınıflı softmax aktivasyonlu bir katman eklenmiştir.

3. Model Eğitimi:
   - Optimizasyon yöntemi olarak Adam optimizer kullanılmıştır.
   - Kayıp fonksiyonu olarak sparse categorical crossentropy kullanılmıştır.
   - Eğitim, 10 epoch boyunca gerçekleştirilmiştir.

4. Model Değerlendirme:
   - Eğitim ve test doğrulukları, F1 skoru, geri çağırma ve kesinlik metrikleri hesaplanmıştır.
   - Karmaşıklık matrisi ile modelin sınıflandırma performansı görselleştirilmiştir.

5. Gelecekteki Geliştirme Önerileri:
   - Daha karmaşık modellerin (örneğin, CNN tabanlı modeller) denenmesi.
   - Veri artırma tekniklerinin kullanılması.
   - Hiperparametre optimizasyonunun daha kapsamlı şekilde yapılması.


## Nasıl Çalıştırılır

1. Gerekli kütüphaneleri yükleyin:
    ```python
    !pip install -r requirements.txt
    ```

2. Projeyi çalıştırmak için Jupyter Notebook'u açın:
    ```bash
    jupyter notebook
    ```

3. `Muhammed_Keskin_fashion_mnist_Aygaz Yapay Zekaya Giriş.ipynb` dosyasını açın ve hücreleri sırasıyla çalıştırın.

## Gereksinimler

- Python 3.x
- TensorFlow
- Keras
- NumPy
- Matplotlib

## Yazar

- **Muhammed Keskin**

