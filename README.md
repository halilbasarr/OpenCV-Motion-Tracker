🚀 OpenCV ile Dinamik Hareket Algılama Sistemi
Bu proje, Python ve OpenCV kütüphanesi kullanılarak geliştirilmiş, gerçek zamanlı bir hareket algılama ve nesne takibi uygulamasıdır. Klasik yöntemlerden farklı olarak, arka planı sürekli güncelleyerek (Weighted Average) değişen ışık koşullarına uyum sağlayabilen daha kararlı bir algoritma kullanılmıştır.

🛠️ Teknik Özellikler
Proje içerisinde aşağıdaki görüntü işleme adımları uygulanmaktadır:

Dinamik Arka Plan Oluşturma: cv2.accumulateWeighted kullanılarak arka planın zamanla güncellenmesi sağlanır. Bu sayede ani ışık değişimlerinden kaynaklanan hatalı algılamalar minimize edilir.

Görüntü Önişleme: Gürültüyü azaltmak için Gaussian Blur ve gri tonlamalı (Grayscale) dönüşüm uygulanır.

Hareket Analizi: cv2.absdiff ile mevcut kare ve arka plan arasındaki fark hesaplanır.

Segmentasyon: Belirlenen eşik değeri (Thresholding) ve genişletme (Dilation) işlemleriyle hareketli bölgeler netleştirilir.

Kontur Takibi: cv2.findContours ile hareket eden nesnelerin sınırları belirlenir ve belirli bir alan eşiğinin (1500 px) üzerindeki hareketler işaretlenir.

📦 Kurulum
Depoyu klonlayın:

Bash
git clone https://github.com/kullanici_adiniz/repo_isminiz.git
cd repo_isminiz
Gerekli kütüphaneleri yükleyin:

Bash
pip install opencv-python numpy
🚀 Kullanım
Uygulamayı başlatmak için terminale şu komutu yazın:

Bash
python motion_detection.py
ESC: Uygulamadan çıkış yapar.

İlk Kare: Uygulama başladığında ilk birkaç saniye arka planı kalibre eder.
