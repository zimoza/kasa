# 🛡️ NesneKasa v2.3 — AI & Görsel Kilit Destekli Güvenli Kasa

**NesneKasa**, fiziksel dünyadaki nesneleri yapay zeka ile tanıyarak dosya kasası kilidine dönüştüren, istemci taraflı (client-side) AES-GCM şifreleme ve bulut senkronizasyonu barındıran modern bir web uygulamasıdır.

Mobil cihazlar (özellikle iOS Safari) ve modern masaüstü tarayıcılar için optimize edilmiştir.

---

## ✨ Özellikler

* 👁️ **Görsel Nesne Kilidi (AI):** **MobileNet (TensorFlow.js)** modeli ile kameraya gösterilen fiziksel nesneler (ör. saat, su şişesi, fincan, kitap) tespit edilir ve kasa/dosya kilit anahtarı olarak atanır.
* 🔐 **Askeri Düzey Şifreleme (AES-256-GCM):** Dosyalar **Web Crypto API** ve **PBKDF2 (150.000 iterasyon)** kullanılarak şifrelenir. Şifresiz hiçbir dosya cihaz dışına çıkmaz.
* 📦 **`.nkasa` Şifreli Paket Paylaşımı:** Dosyaları parola korumalı `.nkasa` zarfları halinde dışa aktarın veya paylaşın. Bu paketler yalnızca NesneKasa ve doğru paket parolası ile açılabilir.
* 💾 **Gelişmiş Yerel Bellek (IndexedDB):** Büyük dosyalar `localStorage` limitlerine takılmadan tarayıcının IndexedDB alanında güvenle saklanır.
* ☁️ **Bulut Senkronizasyonu (Firebase Firestore):** Kasa kimliği (Vault ID) ile cihazlar arası dosya meta verileri senkronize edilir.
* 🔬 **LiDAR / Donanım Farkındalığı:** Destekleyen Apple cihazlarda WebXR / AR derinlik algılama arayüzü ile entegre çalışır.
* 🗑️ **Gizlilik & Oturum Modları:** "Kapatınca Sil" modu aktifken tarayıcı sekmesi kapatıldığı anda tüm yerel önbellek ve dosyalar otomatik temizlenir.

---

## 🚀 Hızlı Başlangıç

NesneKasa tamamen istemci taraflı (front-end) çalışan tek dosyalık bir uygulamadır.

### Gereksinimler
* **HTTPS Bağlantısı:** Tarayıcı güvenlik ilkeleri (Kamera erişimi ve Web Crypto API) gereği sayfanın `https://` protokolü veya `localhost` üzerinde çalışması zorunludur.
* **Modern Web Tarayıcısı:** Chrome, Safari (iOS 14+), Firefox veya Edge.

### Yerel Olarak Çalıştırma

1. Projeyi klonlayın:
   ```bash
   git clone [https://github.com/kullaniciadi/nesnekasa.git](https://github.com/kullaniciadi/nesnekasa.git)
   cd nesnekasa
