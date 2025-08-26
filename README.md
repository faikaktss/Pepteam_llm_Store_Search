<div align="center">
  
<img src="https://cdn-icons-png.flaticon.com/512/3135/3135715.png" width="90" alt="Store Icon"/> 
<img src="https://cdn-icons-png.flaticon.com/512/2721/2721296.png" width="90" alt="AI Icon"/> 
<img src="https://cdn-icons-png.flaticon.com/512/5968/5968705.png" width="90" alt="Database Icon"/> 

# 🏪 Pepteam LLM Store Search

**Doğal dilde, şehir ve hizmet filtreli, vektör tabanlı mağaza arama sistemi**

</div>

---

## ✨ Proje Özeti
**Pepteam LLM Store Search**, mağaza verilerini vektörleştirip **Qdrant vektör veritabanında** depolayan ve kullanıcıdan gelen doğal dildeki sorguları, **şehir** ve **hizmet filtreleriyle** birlikte **semantik** olarak arayabilen modern bir arama altyapısıdır.  

---

## 🚀 Temel Özellikler
- 🏪 Doğal dilde mağaza arama  
- 🧠 Embedding ile vektörleştirme  
- 🗄️ Qdrant vektör veritabanı entegrasyonu  
- 🏷️ Şehir ve hizmet bazlı filtreleme  
- 🔍 Anlam bazlı en yakın sonuçlar ve benzerlik skorları  
- 🚫 Sonuç yoksa veya skor düşükse açıklayıcı mesajlar  

---

## 🧩 Proje Akışı

### 1️⃣ Veri Hazırlama
Mağaza verileri JSON formatında hazırlanır.  
Alanlar:  
- `province` (şehir)  
- `services` (hizmetler, dizi)  
- `notes` (özel notlar)  

### 2️⃣ Vektörleştirme
Her mağaza için özet metin oluşturulur ve **embedding modeliyle vektörleştirilir.**

### 3️⃣ Qdrant’a Yükleme
Oluşan vektörler ve mağaza bilgileri **Qdrant veritabanına toplu olarak yüklenir.**

### 4️⃣ Akıllı Sorgu
- Kullanıcıdan alınan doğal dildeki sorgu embedding ile vektörleştirilir.  
- Qdrant üzerinde arama yapılır.  
- Şehir ve hizmet filtreleriyle arama daraltılabilir.  

### 5️⃣ Sonuçların Sunumu
- En alakalı mağazalar benzerlik skorlarıyla kullanıcıya sunulur.  
- Sonuç yoksa/düşükse → açıklayıcı mesaj gösterilir.  

---

## 🖼️ Örnek JSON Veri
```json
{
  "store_name": "Pepteam İstanbul 1",
  "province": "İstanbul",
  "services": ["Satış", "Teknik Servis"],
  "notes": "Merkez mağaza"
}
🔍 Örnek Sorgu Akışı
Kullanıcı Sorgusu:
"Ankara'da teknik servis veren mağazaları bul"

🔎 Sistem bu sorguyu embedding’e çevirir → Qdrant’ta arar → ilgili mağazaları getirir.


💡 Proje Amacı

Bu proje, klasik anahtar kelime aramalarının ötesine geçerek, kullanıcıların doğal dilde ve anlam bazlı sorgularla mağaza veritabanında arama yapabilmesini sağlar.
Ayrıca şehir ve hizmet filtreleri ile daha hassas sonuçlar sunar.
