# Customer-Experience-Data-Analysis

🔰 Proje Başlığı:
Customer Experience Data Analysis – Müşteri Deneyimi Verisi Üzerine Keşifsel Veri Analizi

🎯 Projenin Amacı:
Bu proje, bir şirkete ait müşteri deneyimi verisinin detaylı bir şekilde incelenmesini, veri kalitesinin değerlendirilmesini, potansiyel modelleme süreçlerine zemin hazırlayacak öngörülerin elde edilmesini amaçlamaktadır. Çalışmada özellikle sayısal ve kategorik değişkenlerin istatistiksel özellikleri, eksik ve aykırı değerlerin varlığı ve veri setinin genel yapısı analiz edilmiştir.

📦 Kullanılan Veri Seti:

-Dosya adı: customer_experience_data.csv

-Gözlem sayısı: ~100.000

-Değişken sayısı: 25 (bir adet tanımlayıcı sütun analiz dışında bırakılmıştır)

-Veri tipleri:

->Sayısal: int64 ve float64 tipindeki sütunlar (örn. Age, Spending_Score, Wait_Time)

->Kategorik: object (örn. Gender, Feedback_Type, Retention_Status)

💻 Kullanılan Teknolojiler ve Kütüphaneler:

-Python (Jupyter Notebook ortamı)

-pandas: Veri işleme ve manipülasyon

-numpy: Sayısal hesaplamalar

-matplotlib & seaborn: Veri görselleştirme

📊 Yapılan İşlemler:

-Veri Setinin Yüklenmesi ve Ön Görünüm

-Veri pandas kullanılarak yüklenmiş ve ilk 5 satırı incelenmiştir.

-Sütun adları ve veri tipleri gözden geçirilmiştir.

-Veri Yapısının İncelenmesi

-Toplam gözlem ve sütun sayısı belirlenmiştir.

-Sayısal ve kategorik değişkenler veri tipine göre ayrılmıştır.

-Sayısal Değişkenlerin İstatistiksel Özeti

-Ortalama, medyan, standart sapma, minimum ve maksimum değerler gibi istatistiksel ölçüler hesaplanmıştır.

Bu özet istatistikler, verilerin genel eğilimi ve yayılımı hakkında fikir vermiştir.

Sayısal Değişkenlerin Dağılımı (Histogramlar)

Tüm sayısal değişkenler için histogram grafikler çizilmiştir.

-Amaç: Dağılımın simetrik olup olmadığı, çarpıklık ve yoğunluk bölgelerinin gözlenmesidir.

-Kategorik Değişkenlerin İncelenmesi

Her kategorik sütun için benzersiz değer sayısı ve en sık tekrar eden değer hesaplanmıştır.

Bu, olası sınıf dengesizliklerinin (örneğin cinsiyet dağılımı veya müşteri memnuniyeti) anlaşılmasını sağlar.

-Kategorik Değişkenlerin Görselleştirilmesi (Barplot)

countplot ile her kategorik değişkenin frekans dağılımı görsel olarak sunulmuştur.

-Eksik Değer Analizi

Her sütundaki eksik değer sayısı ve oranı hesaplanmıştır.

Eksik veri oranları bar grafiği ile görselleştirilmiştir.

Eksik değerler genellikle %5’in altında çıkmıştır; bu da müdahale edilebilir düzeyde olduğunu gösterir.

Aykırı Değer Analizi (IQR Yöntemi)

Her sayısal değişken için çeyrekler arası açıklık (IQR) yöntemi kullanılarak aykırı değerler belirlenmiştir.

Aykırı değer sayısı ve bu değerlerin toplam veriye oranı hesaplanmıştır.

Aykırı Değerlerin Görselleştirilmesi (Boxplot)

Boxplot grafiklerle her sayısal değişkendeki uç değerler görsel olarak tespit edilmiştir.

Özellikle "Flight Distance", "Wait Time" gibi değişkenlerde önemli sapmalar gözlenmiştir.

🔍 Genel Gözlemler ve Değerlendirme:

Veri kalitesi oldukça yüksektir; eksik değer oranı düşüktür.

Sayısal değişkenlerin çoğunda aykırı değerler gözlenmiştir, ancak bu değerler istatistiksel olarak müdahale edilebilir düzeydedir.

Kategorik değişkenlerde bazı sınıflarda dengesizlikler mevcuttur, bu da makine öğrenmesi modellerinde dikkate alınmalıdır.

Veri seti, sınıflandırma modelleri için uygun bir yapıya sahiptir. Özellikle müşteri memnuniyet durumu (“satisfaction” veya benzeri bir hedef değişken) sınıflandırma problemleri için kullanılabilir.

✅ Gelecek Adımlar (Önerilen):

Eksik veriler için median/mean ile imputasyon veya KNNImputer gibi gelişmiş yöntemler kullanılabilir.

Aykırı değerler için Winsorization, log-transform veya outlier removal stratejileri uygulanabilir.

Sayısal değişkenler arasında korelasyon matrisi oluşturulabilir ve yüksek korelasyonlu özellikler tespit edilebilir.

Gerekirse feature engineering adımıyla yeni değişkenler oluşturulabilir.

Modelleme sürecine geçilerek sınıflandırma algoritmaları (Decision Tree, Random Forest, XGBoost, vb.) uygulanabilir.

📎 Lisans ve Bilgi

Bu proje eğitim ve analiz amaçlıdır.

Kullanılan veri seti açık veri kaynaklarından (örneğin Kaggle) temin edilmiştir.
