#  Rice Classification with CNN

Bu projede, beş farklı pirinç türünü sınıflandırmak için bir Convolutional Neural Network (CNN) modeli geliştirdim. 
Veri seti olarak Kaggle’daki Rice Image Dataseti kullandım. Amacım, verilen bir pirinç resminin hangi türe ait olduğunu otomatik olarak tahmin edebilen bir model oluşturmak ve bu süreçte derin öğrenme yöntemlerini uygulamalı olarak öğrenmekti.
Proje sürecinde, öncelikle veri setini yükledim, resimleri ve etiketlerini organize ettim, ardından eğitim ve test setlerine ayırdım. Eğitim sırasında modelin daha iyi genelleme yapabilmesi için veri artırma (data augmentation) teknikleri uyguladım; 
görselleri döndürme, kaydırma, yakınlaştırma ve yatay çevirme gibi işlemlerle modelin farklı durumlara uyum sağlamasını sağladım ve overfitting’i azaltmaya çalıştım.
CNN modelini oluşturduktan sonra, eğitim sırasında modelin doğruluk ve kayıp değerlerini takip ettim. Böylece modelin hem eğitim verisinde ne kadar iyi öğrendiğini hem de yeni veriler karşısında ne kadar genelleme yapabildiğini gözlemleyebildim.

##  Proje Hakkında
- Kullanılan model: CNN (Convolutional Neural Network)
- Girdi boyutu: 100x100, 3 kanallı (RGB)
- Veri: Farklı pirinç türlerinden oluşan resimler
- Eğitim & Doğrulama: Train/Test split
- Amaç: Görselleri doğru şekilde sınıflandırmak ve modelin karar mekanizmasını analiz etmek

##  Kullanılan Teknolojiler
- Python 
- TensorFlow / Keras
- NumPy, Pandas
- Matplotlib, Seaborn
- Scikit-learn

##  Metrikler

Modelin başarısını ölçmek için accuracy (doğruluk), loss (kayıp), confusion matrix ve classification report kullandım. 
Eğitim ve doğrulama doğruluklarını ve kayıplarını grafiklerle görselleştirerek, modelin öğrenme sürecini ve overfitting olasılıklarını değerlendirdim.
Confusion matrix ile modelin hangi pirinç türlerini doğru veya yanlış tahmin ettiğini net bir şekilde görebildim. 
Classification report ise her sınıf için precision, recall ve f1-score değerlerini verdi. Bu sayede modelin genel başarısını ve sınıf bazlı performansını detaylı olarak inceleyebildim. 
Sonuçlar, modelin çoğu pirinç türünde yüksek doğruluk elde ettiğini ve genel olarak başarılı bir sınıflandırma yaptığını gösterdi.


- Accuracy (Doğruluk): %99
- Confusion Matrix: <img width="797" height="633" alt="ConfusionMatrix" src="https://github.com/user-attachments/assets/b16cf67f-1e64-4a78-ad9b-3c6001f025e0" />
- Classification Report: 
                precision   recall   f1-score   support

     Arborio       0.98      0.98      0.98      2996
     Basmati       1.00      0.97      0.99      2995
      Ipsala       1.00      1.00      1.00      2929
     Jasmine       0.96      0.99      0.97      3083
   Karacadag       1.00      0.99      0.99      2997

    accuracy                           0.99     15000
   macro avg       0.99      0.99      0.99     15000
weighted avg       0.99      0.99      0.99     15000


## Ekler

Projede ayrıca, eğitim sırasında modelin en iyi performans gösterdiği halini kaydetmek için ModelCheckpoint kullandım. 
Bu sayede eğitim tamamlandıktan sonra en iyi modeli tekrar yükleyip test verisi üzerinde tahminler yapabiliyorum. 
Bu yöntem, modelin eğitim sırasında aşırı uyum (overfitting) göstermesi durumunda bile en iyi öğrenilen ağırlıkları saklamamı sağladı.

##  Öğrendiklerim
- CNN mimarisini sıfırdan kurmayı
- Modelin overfitting eğilimini nasıl kontrol edeceğimi
- ModelCheckpoint ile en iyi ağırlıkları kaydetmeyi
- Confusion matrix ve classification report ile sonuçları yorumlamayı

## Gelecek Çalışmalar

Bu proje sayesinde CNN mimarisi, veri ön işleme, veri artırma, model eğitimi ve performans değerlendirme konularında pratik deneyim kazandım. 
Modelin performansını grafiklerle ve metriklerle analiz ederek, derin öğrenme sürecini baştan sona gözlemleme fırsatı buldum.
Gelecekte projeyi geliştirmek için, daha büyük ve çeşitli veri setleri ile çalışmayı, modelin hiperparametrelerini optimize etmeyi ve farklı sınıflandırma problemlerine uygulamayı planlıyorum.
Ayrıca, modeli gerçek zamanlı veri üzerinde test edebilecek bir sistem kurmak ve performansını daha geniş bir ölçekte değerlendirmek de projeyi ilerletmek için düşündüğüm adımlar arasında.


## Linkler

Projeye ulaşmak için -> https://www.kaggle.com/code/evinozcelik/rice-classification-cnn
