# Krallığın Yükselişi — Mobil Prototip 0.2

## Telefonda deneme
1. ZIP'i bilgisayarda çıkar.
2. `index.html` dosyasını açarak masaüstünde oynayabilirsin.
3. Telefonda uygulama gibi kurulum için klasörü HTTPS destekli bir statik web sunucusuna yükle.
4. Android Chrome'da adresi açıp menüden "Uygulamayı yükle" / "Ana ekrana ekle" seç.

`file://` üzerinden açıldığında oyun oynanır; PWA çevrimdışı kurulum ve service worker için HTTPS veya localhost gerekir.

## İçerik
- Mobil öncelikli, dikey ekran arayüzü
- Şehir, inşaat, ordu, dünya haritası ve görev sayfaları
- Odun, taş, yiyecek, altın üretimi
- Bina geliştirme ve gerçek zamanlı inşaat sayacı
- Piyade, okçu, süvari eğitimi
- İki yükseltilebilir kahraman
- Düşman kampları ve basit sefer/savaş simülasyonu
- Ana görev zinciri, başarımlar
- Yerel otomatik kayıt, kayıt dışa/içe aktarma
- PWA manifest ve service worker ile çevrimdışı önbellek

## APK hakkında
Bu paket henüz imzalanmış APK değildir. APK üretmek için Android Studio + Android SDK gerekir.
Pratik yol: bu PWA'yı Capacitor ile Android projesine sarmak:
- Node.js LTS ve Android Studio kur.
- Proje klasöründe `npm init -y`
- `npm install @capacitor/core @capacitor/cli @capacitor/android`
- `npx cap init "Krallığın Yükselişi" "com.kralligin.yukselisi" --web-dir .`
- `npx cap add android`
- `npx cap open android`
- Android Studio'da Build > Generate Signed Bundle / APK > APK.
İmzalama anahtarını güvenli sakla. Bu kaynak paketi henüz gerçek cihazlarda test edilmiş değildir.

## Önemli sınırlar
Bu sürüm tek oyunculu prototiptir. Gerçek hesaplar, bulut kayıt, çok oyunculu ittifaklar, sunucu otoritesi, gerçek zamanlı PvP, bildirimler ve mağaza henüz yoktur. Kaynaklar ve savaşlar istemci tarafında çalışır; çevrim içi rekabet için güvenli bir backend gerekir.


## Capacitor başlangıç dosyaları
Paketin kök dizininde `package.json` ve `capacitor.config.json` bulunur.
Windows'ta Node.js LTS kurduktan sonra proje klasöründe terminal aç:
1. `npm install`
2. `npx cap add android`
3. `npx cap sync android`
4. `npx cap open android`
Android Studio'da APK oluştur.
İlk kez Android platformu eklenirken internet bağlantısı gerekir.
