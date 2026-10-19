# Tablino — Yemek Aboneliği Demo

Aliağa / Siteler Mahallesi için geliştirilen **iki rollü** yemek aboneliği web uygulaması demosu.

## Özellikler

**Admin:** Yönetim panosu, gelir/gider grafikleri, fiyat ve katkı payı optimizasyonu, haftalık menü düzenleme, müşteri listesi, tedarikçi listesi, finansal işlem ekleme.

**Müşteri:** Regular / Premium / Exclusive abonelikleri, Standart / Vegan / Sporcu tercihleri, haftalık ana yemek ve yan yemek seçimi, adres yönetimi, ödeme özeti ve simülasyonu.

## Çalıştırma

Node.js 20+ önerilir.

```bash
npm install
npm run dev
```

Terminalde gösterilen adresi tarayıcıda açın (genellikle `http://localhost:5173`).

Üretim dosyalarını oluşturmak için:

```bash
npm run build
```

`dist/` klasörü statik barındırma için hazırdır.

## GitHub'a yükleme

```bash
git init
git add .
git commit -m "Initial Tablino demo"
git branch -M main
git remote add origin https://github.com/KULLANICI_ADINIZ/tablino-demo.git
git push -u origin main
```

GitHub Pages için **Settings > Pages > Build and deployment > GitHub Actions** üzerinden Vite build/deploy iş akışı kurulabilir. Alternatif olarak Vercel veya Netlify'da repoyu içe aktarın: Build command `npm run build`, publish directory `dist`.

## Demo sınırları

- Demo hesapları şifresiz seçilir; **gerçek kimlik doğrulama ve yetkilendirme yoktur**.
- Veriler tarayıcının `localStorage` alanında saklanır; farklı cihazlar arasında senkronize olmaz.
- Kart bilgisi yalnızca maskeli örnek metindir; **gerçek ödeme alınmaz, kart verisi saklanmaz**.
- Dashboard'daki 6 aylık grafik örnek veridir; finans logu ise kullanıcı tarafından düzenlenebilir.
- Haftalık yemek seçimleri bu demo oturumunda saklanır, sayfa yenilendiğinde sıfırlanır. Admin menü/fiyat/finans değişiklikleri kalıcı olarak tarayıcıda saklanır.
- Vegan ve Sporcu filtreleri gösterim amaçlıdır; gerçek alerjen/çapraz bulaşma güvenliği ve beslenme doğrulaması yapılmamaktadır.
- Vergi ve kârlılık hesabı basitleştirilmiştir: satış KDV'si %10, ödeme komisyonu %3 varsayılmıştır; muhasebe görüşü değildir.
- Teslimat, kurye atama, SMS ve tedarikçi bildirimi henüz gerçek servislerle bağlı değildir.

Gerçek kullanıcıya açılmadan önce sunucu, veritabanı, kimlik doğrulama, güvenli ödeme sağlayıcısı, KVKK süreçleri, stok onayı, sipariş son değiştirme saati ve kurye entegrasyonu gerekir.

## Teknolojiler

React 18, Vite, Recharts, Lucide React, CSS. Özel API anahtarı gerektirmez.
