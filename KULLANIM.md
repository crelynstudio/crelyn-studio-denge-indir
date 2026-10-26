# Denge 0.3.0 Beta 1

Türkiye için ücretsiz e-ticaret kâr hesaplayıcı. Tamamen Türkçe, tek işletme ve Türk lirası için geliştirilmiştir. Kaynak kod kapalıdır.

## Açılış

1. `Denge-0.3.0-beta.1-Windows11-x64.zip` dosyasına sağ tıklayıp **Tümünü ayıkla** seçin.
2. Açılan `Denge` klasöründeki **denge.exe** dosyasını çalıştırın. ZIP'in içinden doğrudan çalıştırmayın.
3. `WebView2Loader.dll`, lisans bildirimleri ve `third-party-sources` / `runtime-notices` klasörlerini uygulamanın yanında tutun. Başka bilgisayara taşırken klasörün tamamını kopyalayın.

Yalnız **Windows 11, 64 bit x64** desteklenir. Windows 11'de paket açılışı ve temel kullanım doğrulanmıştır. WebView2 bulunmayan temiz Windows 11 kurulumu henüz gerçek cihazda denenmemiştir. Windows 10, ARM64 ve 32 bit sistemler destek kapsamı dışındadır.

Microsoft **WebView2 Runtime** gerekir; Runtime bu küçük pakete dahil değildir. Bilgisayarda yoksa Microsoft'un [resmî indirme sayfasından](https://developer.microsoft.com/microsoft-edge/webview2/#download-section) **Evergreen Standalone Installer — x64** paketini indirip kurun. Edge tarayıcısının bulunması tek başına yeterli değildir. Denge'yi yeniden açın. İlk indirme/Runtime kurulumu internet gerektirebilir; Runtime kurulduktan sonra hesaplama ve yerel kayıtlar internetsiz çalışır. Node.js, Rust veya geliştirme araçları gerekmez.

Bu deneme paketi dijital olarak imzalanmamıştır. Windows yayıncıyı tanımadığını bildirebilir; indirdiğiniz kaynağı ve SHA-256 değerini doğrulayın. Güvenlik yazılımını kapatmayın.

## Yeni görünüm

Uygulama koyu tema kullanır: kömür siyahı paneller, krem metinler ve amber vurgular. PDF/Excel çıktıları baskıya uygun açık görünümünü korur. Hesaplama kuralları ve kayıt biçimi değişmemiştir.

## İlk hesap

- **Kanal ayarları** bölümünde kendi sözleşmenizdeki komisyon, kargo ve kesintileri girin. Başlangıç değerleri sıfırdır; güncel pazaryeri tarifesi değildir. Özel kanal ekleyebilirsiniz.
- Hesaplayıcıya alış maliyeti, satış fiyatı, adet ve giderleri yazın. Ondalık için virgül veya nokta kullanın; binlik ayırıcı kullanmayın.
- **Hesabı kaydet**, hesap senaryosunu saklar. **Satış olarak kaydet**, gerçekleşmiş satışı raporlara ekler.
- **Satış kayıtları** bölümünde düzenleme ve kısmi iade; **Raporlar** bölümünde filtreleme, Excel ve dikey A4 PDF dışa aktarma bulunur.
- **Kanalları karşılaştır**, mevcut hesabı kayıtlı kanal giderleriyle karşılaştırır.

İadesi olan satışın tutarlarını değiştirmek için önce ilgili iadeleri kaldırın, ardından satışı ve iadeleri doğru değerlerle yeniden düzenleyin.

## Veriler ve güncelleme

Veriler bu klasörde değil, Windows hesabınıza ait `%LOCALAPPDATA%\com.crelynstudio.eticaret\eticaret.db` dosyasında tutulur. Uygulama klasörünü silmek kayıtları silmez. Bu dağıtım taşınabilir çalıştırılabilir pakettir; kayıtları USB üzerinde taşıyan bir veri modu sunmaz.

Güncellemeden önce uygulamadaki **Yedek al** ile JSON yedeği alın, Denge'yi kapatın ve yeni paketi ayrı bir klasöre ayıklayın. Aynı Windows hesabında eski kayıtlar kullanılmaya devam eder. Excel ve PDF tam yedek değildir. JSON geri yükleme mevcut kayıtların yerini alır. Veritabanı ve yedekler şifrelenmez; güvenli saklayın.

Hesap, abonelik, API anahtarı ve bulut sunucusu gerekmez. Telemetri/analitik yoktur. WebView2'nin kendi Microsoft güncelleme davranışı ayrıdır.

## Sınırlar ve lisans

Beta sürümdür; temiz cihaz kurulumu ve tüm Windows/ekran birleşimleri doğrulanmamıştır. Araç muhasebe veya vergi beyanı yerine geçmez. Sonuçlar girdiğiniz oran ve tutarlara bağlıdır. Otomatik pazaryeri bağlantısı, stok takibi, çoklu işletme, bulut eşitleme ve Excel içe aktarma bulunmaz. Tutarların birim başına yuvarlanması faturalarla kuruş farkı oluşturabilir.

Ücretsiz bireysel ve işletme kullanımı için `LICENSE.txt` geçerlidir. Üçüncü taraf hakları `THIRD-PARTY-NOTICES.txt` ve `runtime-notices` altında, MPL bileşenlerinin kaynakları `third-party-sources` altında korunur. Bu bağımsız kaynaklar Denge'nin kaynak kodu değildir.

Crelyn Studio tarafından geliştirildi. [Web sitesi](https://crelynstudio.com) · [İletişim](mailto:info@crelynstudio.com)
