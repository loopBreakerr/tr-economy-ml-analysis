# Makroekonomik Enflasyon Tahminleme ve Pazar Segmentasyonu

## 📌 Projenin Özeti
Bu çalışma, Türkiye ve Avrupa pazarlarındaki makroekonomik dinamikleri analiz eden, baştan sona kendi geliştirdiğim bir Veri Bilimi projesidir. Temel amacım, yeni algoritmaları hızla öğrenme kapasitemi pratiğe dökmek ve karmaşık veri setlerinden somut, uçtan uca çalışabilen proje çıktıları üretebilme yetkinliğimi göstermektir. Proje, sadece veri çekmekle kalmayıp, algoritmalar aracılığıyla enflasyon trendlerini tahmin eder ve ülkeleri yapısal risklerine göre segmentlere ayırır.

## 🚀 Temel Proje Çıktıları
* **Tahminleme Doğruluğu:** XGBoost modeli, Türkiye'nin aylık enflasyonunu **%1.05 MAE (Ortalama Mutlak Hata)** payıyla tahmin ederek "production-ready" bir performans sergilemiştir.
* **Ekonomik Tetikleyiciler:** Analiz sonucunda, Türkiye enflasyonunun ana tetikleyicisinin **Döviz Kuru Getirisi (USD/TRY)** ve **Almanya İthalat Maliyetleri** olduğu algoritmik olarak ispatlanmıştır.
* **Yapısal Segmentasyon:** K-Means kümeleme analizi, Türkiye'yi yüksek volatilite ve risk profili nedeniyle Avrupa sisteminden tamamen ayrışmış tekil bir küme olarak konumlandırmıştır. Almanya, Polonya ve Romanya ise stabil tedarik zinciri çekirdeği olarak aynı kümede toplanmıştır.

## 🛠️ Proje Mimarisi ve Geliştirme Süreci
Proje, Sorumlulukların Ayrılığı (Separation of Concerns) prensibine uygun olarak 3 modüler katmandan oluşmaktadır:
1. **Veri Çekme ve İşleme Katmanı (`Data_Ingestion.ipynb`):** FRED API entegrasyonu ile dinamik veri çekimi, zaman serisi senkronizasyonu ve tek doğru veri kaynağının oluşturulması.
2. **Modelleme Katmanı (`Model_Training.ipynb`):** Verilerin durağanlaştırılarak yüzdelik getirilere dönüştürülmesi, özellik mühendisliği (Feature Engineering) ve XGBoost algoritmasının eğitimi.
3. **Kümeleme Katmanı (`Clustering_Analysis.ipynb`):** Makroekonomik temel performans göstergelerinin (Ortalama Enflasyon, Volatilite, Şok Direnci) çıkarımı ve 3 boyutlu interaktif segmentasyon.

## 📊 Veri Seti Altyapısı
Analizde kullanılan ana veri seti `master_dataset_v2.csv` olup, 2020-2025 dönemini kapsayan Eurostat ve FRED kaynaklı senkronize makroekonomik verileri içermektedir.
