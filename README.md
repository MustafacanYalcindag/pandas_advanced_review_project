# 📈 Pandas Advanced Data Analysis & Reporting Project

Bu proje, Python'ın **Pandas** kütüphanesini kullanarak karmaşık veri setlerini temizleme, birleştirme, analiz etme ve profesyonel raporlara dönüştürme süreçlerini kapsayan ileri düzey bir çalışmadır. Proje, müşteri satış verileri ve bölgesel bilgileri harmanlayarak anlamlı ticari çıkarımlar sunar.

---

## 🛠️ Uygulanan Teknikler ve Kazanımlar

Bu notebook içerisinde aşağıdaki veri bilimi ve analizi teknikleri uygulanmıştır:

### 1. Veri Temizleme (Data Cleaning)
* **Eksik Veri Yönetimi:** `isnull()` ile eksik verilerin tespiti, `fillna()` ile ortalama bazlı doldurma ve `dropna()` ile kritik hatalı kayıtların silinmesi.

### 2. Veri Birleştirme (Merging & Concatenation)
* **Merge:** `CustomerID` gibi ortak sütunlar üzerinden müşteri ve satış tablolarının ilişkisel olarak birleştirilmesi.
* **Concat:** Farklı bölgeleri veya zaman dilimlerini (Mart ve Eylül satışları gibi) içeren tabloların dikey ve yatay olarak uç uca eklenmesi.

### 3. Dinamik Veri İşleme (Transformation)
* **Apply Fonksiyonu:** `apply()` metodu ve özel Python fonksiyonları ile satış tutarlarına göre dinamik olarak "Premium", "Gold", "Standard" gibi kategoriler oluşturma.
* **Matematiksel Hesaplamalar:** Satış tutarlarına otomatik KDV eklenmesi gibi sütun bazlı işlemler.

### 4. İstatistiksel Gruplama (Aggregation)
* **GroupBy Analizi:** Şehir (`City`), Bölge (`Region`) ve Ürün (`Product`) bazlı toplam ve ortalama satış performanslarının raporlanması.

### 5. Veri Depolama (Data Export)
* **Excel Entegrasyonu:** İşlenen ve temizlenen verilerin `to_excel` ile dışa aktarılması ve `read_excel` ile tekrar doğrulanması.

---

## 📂 Dosya Yapısı ve Veri Setleri

| DataFrame | İçerik |
| :--- | :--- |
| `customerDF` | Müşteri isimleri, şehirleri ve yaş bilgileri. |
| `saleDF` | Satış ID, ürün tipi ve satış tutarı bilgileri. |
| `regionsDF` | Şehirlerin bağlı olduğu bölgelerin (Doğu, Kuzey vb.) tanımları. |
| `yenibirlesmisDF` | Tüm tabloların birleştirilmiş ve analize hazır hali. |

---

## 📊 Örnek Rapor Çıktıları
Analiz sonucunda program aşağıdaki gibi kritik iş sorularına yanıt verir:
- **Toplam Satış:** Sisteme kayıtlı tüm başarılı işlemlerin toplam tutarı.
- **En Karlı Şehir & Bölge:** En yüksek ciroyu getiren lokasyonların `idxmax()` ile tespiti.
- **Ürün Performansı:** Hangi ürün grubunun daha yüksek ortalamaya sahip olduğunun analizi.

---

## 🚀 Nasıl Çalıştırılır?

1. Gerekli kütüphaneleri yükleyin:
   ```bash
   pip install pandas numpy openpyxl
