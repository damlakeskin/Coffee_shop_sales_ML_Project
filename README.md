# Coffee_shop_sales_ML_Project (Kahve Dükkanı Satış Verisi Üzerinde Makine Öğrenmesi Projesi)

## Bu projenin amacı, 
Bir kahve dükkanı zincirine ait satış verilerini analiz ederek iş süreçlerini daha verimli hale getirmek, müşteri taleplerini daha iyi anlamak, gelecekteki satışları öngörmek ve hizmet iyileştirmesi ya da olası kampanya düzenlemeleri hakkında altyapı oluşturabilecek verilere ulaşmaktır. Proje, veri bilimi ve makine öğrenmesi tekniklerini kullanarak aşağıdaki hedeflere ulaşmayı amaçlar.

1. **Satış Trendlerinin Analizi**: Belirli zaman dilimlerinde (gün, hafta, ay) satış trendlerinin belirlenmesi, mağaza performanslarının karşılaştırılması ve satışlara etki eden faktörlerin ortaya çıkarılması.
   
2. **Mağaza Performanslarının Karşılaştırılması**: Farklı lokasyonlardaki mağazaların satış performanslarının incelenmesi ve gelirlerine göre mağaza kümelerinin oluşturulması. Bu sayede hangi mağazaların en yüksek performansa sahip olduğu ve hangi mağazaların iyileştirilmesi gerektiği tespit edilecektir.
   
3. **Ürün Kategorileri Üzerinden Gelir Analizi**: Ürün kategorilerinin ve ürünlerin satış performanslarının incelenmesi, hangi kategorilerin ve ürünlerin en fazla gelir getirdiğinin anlaşılması. Bu analiz ile stok yönetimi ve ürün çeşitliliği gibi konularda daha bilinçli kararlar alınması hedeflenmektedir.
   
4. **Sipariş Tahmini**: Gelecekteki satışları ve sipariş miktarlarını tahmin etmek için regresyon modelleri ve sınıflandırma algoritmaları uygulanmıştır. Bu tahminler ile işletmenin tedarik zinciri, stok yönetimi ve operasyonel planlama süreçleri optimize edilebilir.
   
5. **Kümeleme ile Segmentasyon**: KMeans algoritması kullanılarak hem mağazalar hem de ürün kategorileri arasında kümeler oluşturulmuştur. Bu kümeler, farklı mağaza lokasyonları ve ürün kategorileri için daha hedefe yönelik stratejiler geliştirmeyi sağlar.
   
6. **Model Performansının Değerlendirilmesi ve İyileştirilmesi**: Farklı makine öğrenmesi algoritmaları (Doğrusal Regresyon ve Random Forest gibi) kullanılarak satış tahminleri yapılmış ve performansları değerlendirilmiştir. Ayrıca, Grid Search yöntemi ile model hiperparametreleri optimize edilerek model doğruluğu arttırılmıştır.


Bu proje ile hem geçmiş veriler ışığında satışların analizi yapılmış hem de makine öğrenmesi ile geleceğe yönelik tahminler üretilmiştir. Böylece işletmenin daha verimli ve karlı bir şekilde yönetilmesine katkı sağlanması amaçlanmaktadır.

## İçindekiler

- [Veri Seti Hakkında](#veri-seti-hakkında)
- [Proje Adımları](#proje-adımları)
- [Modeller ve Değerlendirmeler](#modeller-ve-değerlendirmeler)
- [Kullanılan Kütüphaneler](#kullanılan-kütüphaneler)
- [Sonuçlar](#sonuçlar)
- [Not](#not)

## Veri Seti Hakkında
Veri seti, kahve dükkanlarındaki satış işlemlerini içermektedir. Aşağıda veri setinde yer alan sütun bilgileri listelenmiştir:

- **Transaction ID**: İşlem için benzersiz kimlik numarası.
- **Transaction Date**: İşlemin gerçekleştiği tarih.
- **Transaction Time**: İşlemin gerçekleştiği saat.
- **Store Number**: Mağazanın kimlik numarası.
- **Store Location**: Mağazanın bulunduğu lokasyon.
- **Unit Number**: Mağaza içindeki birim numarası.
- **Product Category**: Ürünün kategorisi.
- **Product Type**: Ürünün türü.
- **Product Name**: Ürünün adı.
- **Price**: Ürünün fiyatı.
- **Month**: İşlemin yapıldığı ay.
- **Day**: İşlemin yapıldığı gün.
- **Weekday**: İşlemin yapıldığı hafta günü.
- **Hour**: İşlemin yapıldığı saat.

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

## Dataseti Grafiklerinin Genel Sonuçları

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

## Kaggle Linki ve Dataseti Linki

https://www.kaggle.com/code/ayemdamlakeskin/coffee-shop-sales-ml-project
https://www.kaggle.com/datasets/ahmedmohamedibrahim1/coffee-shop-sales-dataset/code

