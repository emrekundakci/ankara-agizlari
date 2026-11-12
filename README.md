# Ankara Ağızları

Ses ve video kayıtlarını araştırmacının kontrolüne hazır parçalara ayırmak, ağız çalışma metni ile standart metni ayrı düzenlemek ve Excel/WAV çıktıları hazırlamak için yerel Mac uygulaması.

Bu depo uygulamanın indirme sayfasını ve kurulum belgelerini içerir. Uygulamanın kaynak kodu burada yayımlanmıyor. Araştırma sesleri, kişisel Excel dosyaları ve tamamlanmış çalışmalar bu depoda bulunmaz.

## Mac uygulamasını indirme

**[Mac uygulamasını indir — DMG, yaklaşık 514 MB](https://github.com/emrekundakci/ankara-agizlari/releases/download/v0.8.1-beta.1/AnkaraAgizlari-0.8.1-AppleSilicon-macOS14.dmg)**

[0.8.1 deneme sürümü ve kurulum dosyaları](https://github.com/emrekundakci/ankara-agizlari/releases/tag/v0.8.1-beta.1) · [Tüm sürümler](https://github.com/emrekundakci/ankara-agizlari/releases)

Sürüm sayfasının **Assets** bölümünde DMG, `KURULUM.txt` ve `SHA256.txt` dosyaları bulunur.

GitHub’ın otomatik oluşturduğu **Source code (zip)** ve **Source code (tar.gz)** dosyaları bu belge deposunun kopyalarıdır; Mac uygulaması değildir.

## Gereksinimler

- Apple M serisi işlemcili Mac: M1, M2 veya sonrası. Intel Mac için hazırlanmadı.
- macOS 14 veya üzeri.
- 16 GB bellek önerilir. 8 GB cihazlarda yeterlilik doğrulanmadı.
- İlk kurulum ve çalışma için yaklaşık 15 GB boş alan önerilir; kayıtlar ayrıca alan kullanır.
- İlk ses çözümlemesinde yaklaşık 3,08 GB Whisper modeli indirilir. İnternet gerekir; model sonraki kayıtlar için bu Mac’te saklanır.

Python, FFmpeg veya Audacity kurmak gerekmez. Ses çözümleme bu Mac’te yapılır; kayıtlar GitHub’a ya da çevrim içi bir yazıya aktarma hizmetine gönderilmez.

## Kurulum

1. DMG dosyasını indirip açın.
2. İçindeki **KUR.command** dosyasına çift tıklayın.
3. Kurulum açıklamasını okuyup **Kur** düğmesiyle onaylayın. Uygulama kullanıcının `~/Applications` klasörüne kurulur.

`KUR.command` açılmazsa veya **Yine de Aç** seçeneği görünmezse, DMG açıkken Terminal’de şu satırı çalıştırın:

```sh
/bin/bash "/Volumes/AnkaraAgizlari081/KUR.command"
```

Kurulum yardımcısı, onayınızla yalnız bu paketten oluşturduğu yeni uygulama kopyasını indirme işaretini taşımadan kurar. Mac’in genel güvenlik ayarlarını değiştirmez. Mevcut bilinen uygulama açıksa önce kaydetmenizi ve kapatmanızı ister; kapalı eski uygulamayı silmeden yedekler. Araştırma dosyalarına işlem yapmaz.

Paket ad-hoc imzalıdır; **Apple Developer ID imzası ve Apple noter onayı yoktur**. Bu nedenle ilk açılışta macOS uyarısı görülebilir. Kurum tarafından yönetilen cihazdaki kısıtlamalar için kurumun teknik desteğine başvurun. [Apple’ın ilk açılış açıklaması](https://support.apple.com/102445).

Ayrıntılı adımlar: [KURULUM.txt](KURULUM.txt). DMG içinde çevrimdışı açılabilen **BASLA.html** rehberi de bulunur.

## Deneme sürümünün durumu

**0.8.1 bir deneme sürümüdür.** Paylaşım paketinin bileşenleri macOS 14/arm64 hedefleri ve paket bütünlüğü açısından kontrol edildi. M2 Pro/macOS 26.6.2 üzerinde kısa Türkçe deneme sesinin yazıya aktarılması, arayüz, kurulum ve Excel/WAV ZIP çıktıları sınandı.

Fiziksel bir M1/macOS 14 bilgisayarda doğrulama yapılmadı. İlk bursiyer denemesinde ses işleme süreci hata ile sonlandı; nedenini belirlemek için hata kaydı bekleniyor. Bu nedenle önce kısa bir kayıtla deneme yapın.

Otomatik metin ön dökümdür; ağız özellikleri ve zaman sınırları dinleyerek kontrol edilmelidir. Konuşurlar elle seçilir. Programın konuşur kimliğini otomatik doğru belirlediği varsayılmamalıdır.

## Çalışma ve çıktı

Ses/video seçip kayıt kodunu yazın; ilçe, köy ve konuşur bilgilerini **Kayıt bilgileri** bölümünden girin. **Konuşurlar → Konuşur ekle** ile K3, K4 ve devamını ekleyebilirsiniz.

**Sesi böl ve yazıya aktar** sonrasında segmentleri dinleyin; ağız ve standart metinleri ayrı düzenleyin. Düzenli olarak **Düzeltmeleri kaydet** veya **⌘S** kullanın. **Çalışmayı bitir ve çıktıları al**, ortak Excel ve tüm WAV parçalarını içeren ZIP üretir.

Çalışmalar `~/Library/Application Support/Ankara Agizlari 0.8.1/outputs` altında saklanır. Yedeklemek için ilgili çalışma klasörünün tamamını kopyalayın. Yalnız Excel dosyası uygulamada devam etmek için yeterli değildir. Ekip üyelerinin çalışmaları otomatik eşitlenmez.

## Geri bildirim

Sorunu anlatırken macOS sürümünü, bellek miktarını ve hata mesajını belirtin. Araştırma seslerinizi veya kişisel Excel dosyalarınızı herkese açık olarak paylaşmanız gerekmez.

Paketin içerdiği üçüncü taraf bileşenlerin lisansları DMG içindeki **LISANSLAR** klasöründedir.
