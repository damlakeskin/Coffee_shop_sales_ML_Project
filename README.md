# Coffee_shop_sales_ML_Project
## Proje Adımları
1. **Veri Yükleme ve İnceleme**: `pandas` ve `openpyxl` kullanılarak veri seti yüklendi ve genel bir inceleme yapıldı.
2. **Veri Temizleme**: Eksik veya tekrar eden veriler kontrol edildi ve temizlendi.
3. **Etiketleme**: Kategorik veriler `LabelEncoder` kullanılarak etiketlendi.
4. **Korelasyon Analizi**: Özellikler arasında korelasyon hesaplanarak ısı haritası oluşturuldu.
5. **Makine Öğrenmesi Modelleri**: `Linear Regression`, `Random Forest Classifier` gibi modellerle eğitim yapıldı ve tahminler değerlendirildi.
6. **Kümeleme Analizi**: KMeans algoritmasıyla mağaza ve ürün kategorileri kümelendi.
7. **Grid Search ile Optimizasyon**: `GridSearchCV` kullanılarak hiperparametre optimizasyonu yapıldı.

## Modeller ve Değerlendirmeler
Projede kullanılan bazı modeller ve performans değerlendirme metrikleri aşağıda listelenmiştir:

- **Doğrusal Regresyon (Linear Regression)**
  - Mean Squared Error (MSE)
  - Mean Absolute Error (MAE)
  - Root Mean Squared Error (RMSE)
  
- **Random Forest Classifier**
  - Accuracy
  - R-squared
  - Confusion Matrix
  
- **K-Means Kümeleme**
  - Inertia (WCSS)
  - Silhouette Score

## Kullanılan Kütüphaneler
Proje boyunca aşağıdaki Python kütüphaneleri kullanılmıştır:

NumPy: Matematiksel işlemler ve dizi işlemleri için kullanılır.
Pandas: Veri işleme ve analiz işlemlerini gerçekleştirmek için kullanılır. CSV ve Excel dosyalarını işlemek için idealdir.
Scikit-learn: Makine öğrenmesi algoritmalarını (linear regression, random forest, k-means clustering, vb.) uygulamak ve değerlendirmek için kullanılır.
Seaborn & Matplotlib: Veri görselleştirmeleri oluşturmak için kullanılır. Bar grafikleri, ısı haritaları, scatter plotlar vb. görseller oluşturulmuştur.
Openpyxl: Excel dosyalarının işlenmesi ve okunması için kullanılır.
StandardScaler: Verilerin standardize edilmesi için kullanılır, özellikle K-means kümeleme algoritmasında.
GridSearchCV: Model optimizasyonu için kullanılır, parametre ayarlaması yapılır.
ConfusionMatrixDisplay: Random Forest sonuçlarını görselleştirmek için kullanılır.

## Sonuçlar

## Dataseti Grafiklerinin Genel Sonucu

- İncelenen veriler 3 farklı lokasyonda mağazası bulunan bir Kahve Dükkanına aittir. 1 Ocak 2023 tarihi ile 30 Haziran 2023'e kadar veriler mevcuttur.
Ocak ayında 2000 birim ile başlayan kazanç, haziran ayının sonuna kadar ara ara düşüş yaşasa da sürekli yükselme eğilimindedir ve haziran sonunda 6000 birime ulaşmıştır.
Şubat ayında ufak bir düşüş yaşanmıştır fakat bu düşüşün şubat ayının diğer aylardan daha az gün sayısına sahip olması ile bağıntılı olduğunu düşünülmüştür.
- Özellikle sabah saat 7:00 ile 10:00 arasında gelirlerde yoğunluk mevcuttur. Bunun yanında Salı günleri bu yoğunluk çok daha fazladır. Saat 11:00 ve 18:00 arasında ortalama bir gelir dağılımı mevcut iken saat 6:00 ve 19:00 için düşük gelirden, saat 20:00 için de en düşük gelir seviyesinden bahsedilebilir.
- 3 ayrı lokasyonda bulunan mağazalar için benzer gelirlere sahip oldukları söylenebilir.
- Bu mağazalarda en çok satılan 10 ürün çeşidi 5 kahve ürünü, 3 çay ürünü, 1 içilebilir çikolata ürünü ve Scone içerir. Scone ürünü çoğunlukla kahve ürününün eşlikçisi olarak kabul edildiği için bu da bize bu mağazanın kahve bazlı ürünlerinin diğer ürünlere oranla daha fazla satıldığını gösteriyor olabilir.
- Verilen siparişlerin çoğunluğunun 0 ile 5 gelir aralığı içinde olduğu görülmüştür. Bu mağazanın gelirinin çok büyük bir yüzdesini 5 birim ve daha altındaki satışlarından elde ettiği görülmüştür ve kampanya stratejisi uygun görülmüştür.
- Siparişlerin çoğunun az sayıda ürün içerdiği gözlemlenmiştir. Kampanya stratejisi önerilmiştir.
- Konum bazlı satlışların saatler üzerinde dağılımı incelenip her bir lokasyonda bulunan mağaza için yorumlar yapılmıştır.
- Korelasyon matrixi oluşturulmuştur. Çıktıları, bazı ürünlerin daha az satılıyor olabileceği, ürün fiyatı arttıkça sipariş miktarının azaldığı yönündedir.
- Ürün bazlı kümelenen değerler ile bu mağazaların en fazla gelir sağladığı ürün kategorisi "Drinking Chocolate"dır.

## Unsupervised ve Supervised Learning Sonuçları

- Lineer Regresyon(LinearRegression) ve Rastgele Orman Sınıflandırıcısı(RandomForestClassifier) algoritması ve K-Means(K-Ortalama) Kümeleme Algoritması Seçilmiştir.
- Lineer Regresyon(LinearRegression) ve Rastgele Orman Sınıflandırıcısı(RandomForestClassifier) algoritması modellerinde elde edilen sonuç Hiperparametre sonuçlarına fazlasıyla yakındır.
- Hiperparametre çıktıları karşılaştırılmış ve Lineer Regresyon(LinearRegression) algoritmasının daha doğru ve makul bir model sağladığı sonucuna varılmıştır.

## Not

Bu kısımda proje sürecini kendim için yorumlayacağım.
Öncelikle söylemem gerekiyor ki bu projeye başlarken sadece giriş seviyesinde bir Phyton bilgisine sahiptim. ML hakkında ise en ufak bir fikre sahip değildim, kendimi denemek ve kendi birikimim(Endüstriyel Tasarım çıkışlıyım.) ile en ufak bir benzerliğe sahip olmayan bu alanda kendime meydan okumak istedim.
Göker Hocamın ders anlatım videosunu dinleyerek daha genel bir bilgi anlayışına sahip oldum ve devamında sunulan kaynaklar, örnek çalışmalar ve yapay zekanın yardımı ile kendimi geliştirdim bunların sonucunda da projemi sonuçlandırdım.
Bu readme dosyası dışında .ipynb uzantılı dosya projemi değerlendirecek ya da okuyacak kişi ve kişiler için değil, öğrenim sürecimde neler yaptığımın doğrultusunda aslında ders çalışır gibi kendime aldığım notlardır. Bu noktada istenilenden daha açıklayıcı ya da fazla uzun olmuş olabilir.
Verilen sürenin benim için yeterli olduğunu düşünüyorum. Mentörlerimiz de oldukça bilgili ve ilgiliydi. Herkese ayrı ayrı emekleri doğrultusunda teşekkür ederim buradan, bu farklı deneyim için özellikle. Uğurcan hocam ve Sima hocam da sorularımı yanıtlayarak bana çok yardımcı oldular, buradan onlara ayrı bir teşekkürler geçmek istedim.
## Kurulum
Projeyi kendi bilgisayarınızda çalıştırmak için aşağıdaki adımları takip edebilirsiniz:

1. Bu repoyu klonlayın:
   ```bash
   git clone https://github.com/kullaniciadi/kahve-dukkani-satis-verisi.git
