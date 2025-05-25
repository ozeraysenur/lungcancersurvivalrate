# 🧠 Akciğer Kanseri Hayatta Kalma Tahmini – Makine Öğrenmesi Projesi

Bu proje, **Akbank – Makine Öğrenmesi Bootcamp: Yeni Nesil Proje Kampı** kapsamında geliştirilmiştir.  
Amaç, akciğer kanseri teşhisi almış bireylerin **hayatta kalıp kalamayacaklarını** bazı demografik ve klinik verilere bakarak **makine öğrenmesi algoritmalarıyla tahmin etmektir**.

---

## 📌 Proje Özeti

Kanser gibi ciddi hastalıklarda, hayatta kalma ihtimalinin doğru tahmin edilmesi tedavi planlarını şekillendirmek açısından büyük önem taşır. Bu proje ile sağlık verilerini analiz ederek güçlü bir tahmin sistemi geliştirmeyi hedefledim.

Problemin tipi:  
🎯 **İkili Sınıflandırma (Binary Classification)**  
- `1` → Hayatta kaldı  
- `0` → Hayatta kalamadı

---

## 🧪 Kullanılan Teknolojiler

- Python 3.11
- pandas, numpy
- matplotlib, seaborn
- scikit-learn
- xgboost, lightgbm
- imbalanced-learn
- Jupyter Notebook / Kaggle Notebooks

---

---

## 🔍 Proje Aşamaları

### 1. Keşifsel Veri Analizi (EDA)
- Sınıf dengesizliği analizi
- Sayısal ve kategorik değişkenlerin dağılımı
- Aykırı değer analizi (özellikle `age`, `bmi`)

### 2. Veri Ön İşleme
- Eksik değer kontrolü
- Kategorik değişkenlerin Label Encoding / One-Hot Encoding ile sayısallaştırılması
- Sayısal sütunların StandardScaler ile ölçeklenmesi
- `treatment_duration_days` gibi yeni zaman bazlı özellikler oluşturulması

### 3. Özellik Mühendisliği (Feature Engineering)
- `age_squared`, `age_cubed`, `bmi_squared` gibi polinomik özellikler
- `total_risk_score`: sağlık geçmişi ve risk faktörlerinden hesaplanan toplam risk puanı
- `treatment_intensity`: tedavi süresi / kanser evresi
- Etkileşimli özellikler: `age * cancer_stage`, `bmi * smoking_status`

### 4. Model Eğitimi ve Karşılaştırma
Aşağıdaki modeller eğitilmiş ve performansları karşılaştırılmıştır:

| Model               | Doğruluk (Accuracy) | Precision | Recall | F1-Score |
|---------------------|---------------------|-----------|--------|----------|
| ✅ **XGBoost**        | **0.7798**           | **0.8283**  | 0.7798 | **0.6833** |
| Logistic Regression | 0.7798              | 0.6080    | 0.7798 | 0.6833   |
| Naive Bayes         | 0.7798              | 0.6080    | 0.7798 | 0.6833   |
| Gradient Boosting   | 0.7798              | 0.6080    | 0.7798 | 0.6833   |
| Random Forest       | 0.7796              | 0.6528    | 0.7796 | 0.6833   |
| Decision Tree       | 0.6437              | 0.6561    | 0.6437 | 0.6497   |

---
📎 Kaggle Notebook:  
Projenin tüm adımlarını içeren Jupyter defterime aşağıdaki bağlantıdan ulaşabilirsiniz:  
👉 [https://www.kaggle.com/code/ayenurzer/lung-cancer-ml-project](https://www.kaggle.com/code/ayenurzer/lung-cancer-ml-project)



