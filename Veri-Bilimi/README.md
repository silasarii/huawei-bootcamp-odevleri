# 📊 Veri Bilimi 

Bu klasör, **Huawei Student Developers** ve **Türkiye Yapay Zeka Akademisi** iş birliğiyle düzenlenen Veri Bilimi ve Makine Öğrenmesi Bootcamp'inin 2. haftası kapsamında tamamlanan Veri Analizi, Veri Temizleme, Keşifçi Veri Analizi (EDA) ve Veri Hikayeleştirme ödevlerini içermektedir.

---

## 📂 İçerik ve Dosya Yapısı

| Dosya Adı | Konu / Açıklama |
| :--- | :--- |
| `ara_odev.ipynb` | Veri seti yükleme, eksik veri yönetimi, tip dönüşümleri, metin/kategori standartlaştırma, aykırı/hatalı değer temizleme ve temel EDA işlemleri. |
| `final_odevi.ipynb` | Kategori, şehir, ödeme türü, zaman serisi ve çapraz kırılımlar (şehir-kategori) üzerinden iş odaklı EDA, görselleştirme ve stratejik yorumlama. |

---

## 📌 Ödev Detayları ve Kapsamı

### 📄 1. Ara Ödev (`ara_odev.ipynb`)
Veri setinin temizlenmesi ve analize hazır hale getirilmesi adımlarını kapsar:
1. **Veri Seti Tanıma:** İlk/son satırlar, boyut bilgisi, `info()` ve `describe()` özetleri; sayısal ve kategorik sütun ayrımı.
2. **Eksik Veri (Missing Data):** Eksik veri oranlarının tespiti, ilk 20 eksik satırın filtrelenmesi.
   - `indirim_orani` & `musteri_puani` $\rightarrow$ Medyan (Median) ile doldurma.
   - `odeme_turu` & `musteri_tipi` $\rightarrow$ Mod (Mode) ile doldurma.
3. **Veri Tipleri & Sütun Üretimi:** `siparis_tarihi` tarih tipine dönüştürülerek `siparis_yili`, `siparis_ayi`, `siparis_gunu`, `haftanin_gunu` sütunlarının türetilmesi.
4. **Tekrarlayan Kayıtlar (Duplicates):** Duplicate verilerin tespiti ve veri setinden kaldırılması.
5. **Metin & Kategori Standartlaştırma:** `sehir` ve `kategori` sütunlarındaki yazım hatalarının/tutarsızlıklarının (`İstanbul`, `istanbul`, `ev yaşam`, `ev&yaşam` vb.) tek formata getirilmesi.
6. **Mantıksal Hata & Aykırı Değer Analizi:**
   - Mantıksal hatalı kayıtların (`birim_fiyat <= 0`, `toplam_tutar <= 0`, `teslimat_gunu < 0`, `musteri_puani > 5`) tespiti ve temizlenmesi.
   - `birim_fiyat` sütunu için **IQR (Interquartile Range)** yöntemi ile alt/üst sınır tespiti ve aykırı değer sayımı.
7. **Keşifçi Veri Analizi (EDA):** `toplam_tutar` histogram/boxplot grafikleri, kategori dağılımları (`value_counts`), ödeme türü `count plot` ve temel metrik yorumlamaları.

---

### 📄 2. Final Ödevi (`final_odevi.ipynb`)
Veriden iş stratejileri ve aksiyon alınabilir kararlar çıkarma odaklı analizler:
1. **Kategori Bazlı Performans & Memnuniyet:** Sipariş sayısı, toplam gelir, ortalama tutar, müşteri puanı ve teslimat sürelerinin analizi. Bar plot ile gelir ve memnuniyet kıyaslaması.
2. **Şehir Bazlı Potansiyel Analizi:** Şehirlerin gelir sıralaması, en güçlü 5 şehir görselleştirmesi ve *"Müşteri puanı yüksek ancak geliri düşük"* olan büyüme adayı şehirlerin tespiti.
3. **Ödeme Türü & Müşteri Davranışı:** En yüksek gelir üreten ödeme yöntemi ile en yüksek müşteri memnuniyeti sağlayan ödeme yönteminin karşılaştırmalı analizi.
4. **Zaman Serisi & Satış Eğilimi:** Ay bazında sipariş sayısı ve gelir değişimi (Line Plot). Sipariş artışı ile gelir artışının paralellik gösterip göstermediğinin analizi.
5. **Şehir - Kategori Çapraz Analizi:** En güçlü 10 şehir-kategori kombinasyonunun tespiti ve pazarlama/kampanya stratejisi açısından iş diliyle yorumlanması.

---


## 🛠️ Kullanılan Teknolojiler

- **Python**
- **Pandas & NumPy:** Veri manipülasyonu, temizleme, gruplama (`groupby`) ve özet tablo oluşturma.
- **Matplotlib & Seaborn:** Veri görselleştirme (Bar plot, Line plot, Box plot, Count plot, Histogram).
