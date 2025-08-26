🏪 Pepteam LLM Store Search
<div align="center"> <img src="https://cdn-icons-png.flaticon.com/512/3135/3135715.png" width="90" alt="Store Icon"/> <img src="https://cdn-icons-png.flaticon.com/512/2721/2721296.png" width="90" alt="AI Icon"/> <img src="https://cdn-icons-png.flaticon.com/512/5968/5968705.png" width="90" alt="Database Icon"/> </div>
✨ Proje Özeti
Pepteam LLM Store Search, mağaza verilerini vektörleştirip Qdrant vektör veritabanında depolayan ve kullanıcıdan gelen doğal dildeki sorguları, şehir ve hizmet filtreleriyle birlikte semantik olarak arayabilen modern bir arama altyapısıdır.

🚀 Temel Özellikler
Doğal Dil Sorgusu: Kullanıcıdan gelen serbest metinle arama.
Vektörleştirme: Mağaza açıklamaları embedding modeliyle vektörlere dönüştürülür.
Qdrant Entegrasyonu: Tüm vektörler Qdrant vektör veritabanında saklanır.
Filtreleme: Şehir ve hizmet bazlı filtreleme desteği.
Anlamlı Sonuçlar: En alakalı mağazalar ve benzerlik skorlarıyla sonuçlar.
Açıklayıcı Hata Mesajları: Sonuç yoksa veya skor düşükse kullanıcıya nedenini açıklar.
🧩 Proje Akışı
Veri Hazırlama:
Mağaza verileri JSON formatında hazırlanır.

province (şehir)
services (hizmetler, dizi)
notes (özel notlar)
Vektörleştirme:
Her mağaza için özet metin oluşturulur ve embedding modeliyle vektörleştirilir.

Qdrant’a Yükleme:
Oluşan vektörler ve mağaza bilgileri Qdrant veritabanına toplu olarak yüklenir.

Akıllı Sorgu:
Kullanıcıdan alınan doğal dildeki sorgu, embedding ile vektörleştirilir ve Qdrant’ta arama yapılır.
Şehir ve hizmet filtreleriyle arama daraltılabilir.

Sonuçların Sunumu:
En alakalı mağazalar, benzerlik skorlarıyla birlikte kullanıcıya sunulur.
Sonuç yoksa veya skor düşükse, kullanıcıya nedenini açıklayan mesaj gösterilir.

🖼️ Örnek JSON Veri
🔍 Örnek Sorgu Akışı
🛠️ Kullanılan Teknolojiler
Node.js
Qdrant
@xenova/transformers
prompt-sync
uuid
💡 Proje Amacı
Bu proje, klasik anahtar kelime aramalarının ötesine geçerek, kullanıcıların doğal dilde ve anlam bazlı sorgularla mağaza veritabanında arama yapabilmesini sağlar.
Ayrıca, şehir ve hizmet gibi alanlarda filtreleme ile daha hassas sonuçlar sunar.
