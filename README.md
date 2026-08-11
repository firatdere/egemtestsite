# Egemdent — İmplant Tedavisi Landing Page

Tek dosyalık, framework gerektirmeyen (saf HTML + CSS + JS) bir landing page.
GitHub Pages, Netlify veya herhangi bir statik hosting'e doğrudan yüklenebilir.

## Klasör Yapısı

```
.
├── index.html              → Ana sayfa (tüm CSS ve JS dosyanın içinde)
└── assets/
    └── gozde-orhan-mut.jpg → Doktor fotoğrafı
```

## GitHub Pages'e Yayınlama (adım adım)

1. GitHub'da yeni bir repo oluşturun (Public).
2. Bu klasördeki **tüm dosyaları** (index.html + assets klasörünü olduğu gibi,
   klasör yapısını bozmadan) repoya yükleyin.
   - Dosya adının `index.html` olması şart — GitHub Pages varsayılan olarak bunu arar.
   - `assets` klasörünü de aynı üst dizine yükleyin, içindeki fotoğrafla birlikte.
3. Repo içinde **Settings → Pages** sekmesine gidin.
4. **Branch**: `main`, klasör: `/ (root)` seçip **Save**'e basın.
5. 1-2 dakika içinde şu formatta bir link aktif olur:
   `https://kullaniciadiniz.github.io/repo-adi/`

### Kendi alan adınızı bağlamak isterseniz
Aynı Pages ayarlarında **Custom domain** kutusuna alan adınızı yazın, alan adı
sağlayıcınızda GitHub'ın verdiği DNS kayıtlarını (CNAME/A) ekleyin. GitHub
otomatik ücretsiz SSL sertifikası oluşturur.

## Yayına Almadan Önce Tamamlanması Gerekenler

Sayfa teknik olarak hazır, ancak aşağıdaki içerikler markaya ait **gerçek
verilerle** güncellenmeli:

- [ ] **Telefon numarası kararı** — Şu an "Ara" butonları `+90 216 999 46 55`
      sabit hattına, WhatsApp butonları `+90 530 181 34 44` cep numarasına
      gidiyor. Tek numara mı, iki ayrı numara mı kullanılacak netleşmeli.
      (`index.html` içinde `tel:` ve `wa.me` ile başlayan linkleri arayıp
      değiştirin.)
- [ ] **Gerçek hasta yorumları** — "Yorumlar" bölümündeki isimler (Elif K.,
      Mehmet Y., Ayşe D.) ve yorum metinleri kurgusaldır, KVKK onaylı gerçek
      yorumlarla değiştirilmeli.
- [x] ~~Klinik / tedavi odası fotoğrafları~~ — Tamamlandı: Kliniğimizi Tanıyın
      slider'ında giriş, bekleme alanı/resepsiyon ve tedavi odası gerçek
      fotoğraflarla güncellendi.
- [ ] **Sosyal medya hesapları** — Footer'daki Instagram/Facebook linkleri
      örnek adres (`instagram.com/egemdent` vb.), gerçek hesap linkleriyle
      güncellenmeli.
- [ ] **Google Maps koordinatları** — JSON-LD şemasındaki enlem/boylam
      (`latitude`/`longitude`) yaklaşık değerdir, Google Business
      Profile'daki kesin konumla güncellenmeli.
- [ ] **Alan adı** — GitHub Pages'in ücretsiz linkiyle mi devam edilecek,
      yoksa kendi alan adı mı (örn. egemdent.com) alınacak.

## Yayınlandıktan Sonra

- Google Business Profile'daki adres/telefon/çalışma saatleri sayfadakiyle
  **birebir aynı** olmalı (yerel SEO güven sinyali için kritik).
- [Google Search Console](https://search.google.com/search-console)'a ekleyip
  dizine gönderin.
- Sayfadaki iletişim formu kaldırıldığı için tüm dönüşümler WhatsApp/Ara
  butonları üzerinden gerçekleşiyor — bu butonların linklerini yayından önce
  son bir kez test edin.

## Teknik Notlar

- Harici bağımlılık: yalnızca Google Fonts (Space Grotesk + Inter) CDN
  üzerinden yükleniyor, internet bağlantısı gerektirir.
- Sayfa içinde `schema.org` JSON-LD yapılandırılmış verisi (Dentist +
  FAQPage) bulunur — arama motorları ve yapay zekâ yanıt motorları için.
- Build/derleme süreci yoktur; dosyayı doğrudan tarayıcıda açarak da yerel
  önizleme yapabilirsiniz.
