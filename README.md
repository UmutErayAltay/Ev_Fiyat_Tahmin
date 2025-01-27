# Ev Fiyat Tahmin Projesi

Bu proje, Türkiye'deki ev fiyatlarını tahmin etmek amacıyla geliştirilmiştir. Proje, çeşitli makine öğrenimi yöntemlerini kullanarak evlerin fiyatlarını etkileyen faktörleri analiz eder ve tahmin modelleri oluşturur.

## İçindekiler
- [Kurulum](#kurulum)
- [Kullanım](#kullanım)
- [Veri Seti](#veri-seti)
- [Modelleme Süreci](#modelleme-süreci)
- [Sonuçlar](#sonuçlar)
- [Katkıda Bulunma](#katkıda-bulunma)
- [Lisans](#lisans)

---

## Kurulum

Bu projeyi kullanmak için aşağıdaki adımları takip edebilirsiniz:

1. Bu projeyi klonlayın:
    ```bash
    git clone https://github.com/UmutErayAltay/Ev_Fiyat_Tahmin.git
    cd Ev_Fiyat_Tahmin
    ```

2. Gerekli Python kütüphanelerini yüklemek için aşağıdaki komutu çalıştırın:
    ```bash
    pip install -r requirements.txt
    ```

## Kullanım

1. **Veri Ön İşleme:** 
   - `data` klasörüne ilgili veri setinizi yerleştirin.
   - Gerekli veri temizleme ve ön işleme işlemleri `data_preprocessing.py` dosyasında gerçekleştirilmiştir.

2. **Model Eğitimi:**
   - `model_training.py` dosyasını çalıştırarak modeli eğitebilirsiniz:
     ```bash
     python model_training.py
     ```

3. **Tahmin Yapma:**
   - Eğitilen model ile tahmin yapmak için `predict.py` dosyasını kullanabilirsiniz:
     ```bash
     python predict.py --input your_input_data.csv
     ```

## Veri Seti

Bu proje, ev fiyatlarını tahmin etmek için [özel bir veri seti](data/) kullanır. Veri setinde aşağıdaki özellikler bulunur:
- **Alan (metrekare):** Evin büyüklüğü.
- **Oda Sayısı:** Evin odalarının sayısı.
- **Konum:** Evin bulunduğu şehir/ilçe bilgisi.
- **Yaş:** Evin yaşı.
- **Kat:** Evin bulunduğu kat bilgisi.

**Not:** Veri setini kullanmadan önce anonimlik ve gizlilik kurallarına uyduğunuzdan emin olun.

## Modelleme Süreci

1. **Veri Keşfi:**
   - Veri setindeki eksik ve aykırı değerler incelenmiş ve gerekli dönüşümler yapılmıştır.
2. **Özellik Mühendisliği:**
   - Yeni değişkenler türetilmiş ve gereksiz değişkenler çıkarılmıştır.
3. **Model Seçimi:**
   - Çeşitli makine öğrenimi algoritmaları (örneğin, Lineer Regresyon, Random Forest, XGBoost) test edilmiştir.
4. **Değerlendirme:**
   - Modeller çeşitli metriklerle (örneğin, R^2, RMSE) değerlendirilmiştir.
