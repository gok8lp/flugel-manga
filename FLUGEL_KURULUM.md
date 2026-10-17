# Flugel Manga — telefon kurulumu

Bu depo [Koharia](https://github.com/Mister-album/Koharia) kaynak kodundan türetilmiş,
ayrı bir Android APK'sıdır. Tarayıcı kısayolu değildir: Komga ve Kavita için uygulama
içindeki sunucu bağlantılarını ve yerel okuyucuları kullanır. Kaynak lisansı `LICENSE`
ve atıflar `NOTICE` içinde korunur.

## Kütüphaneyi bağlama

1. GitHub Releases bölümündeki **test APK**'sını Android telefona kur.
2. Uygulamada bağlantı ekle → **Komga**. Genel sunucu adresi olarak
   `https://manga.gokalpgoksu.com` gir. Komga hesabının kullanıcı/parolasını
   veya Komga API anahtarını uygulamanın kendi ayar ekranına gir.
3. İstersen ikinci bağlantı olarak **Kavita** ekle. Adres
   `https://ln.gokalpgoksu.com`; Kavita profilindeki üçüncü taraf istemci
   **Auth Key** değerini uygulamaya gir. Bu bağlantı EPUB romanlar içindir.
4. Sunucuya bağlanırken kitaplıkları seç; manga ve Re:Zero romanları farklı
   raflarda görünmelidir. Kitaplık içeriği, tarama ve okuma ilerlemesi sunucu
   hesabının izinlerine bağlıdır.

Adresler Cloudflare Tunnel üzerinden halihazırda yayımlanıyor. Uygulama
Cloudflare web sayfasını açmaz; sunucuların API'lerine HTTPS ile bağlanır.
Cloudflare Access giriş ekranı bu adreslere sonradan eklenirse API istekleri
çalışmayabilir; o durumda uyumlu erişim yöntemi ayrıca tasarlanmalıdır.

Bu açık depoda ve APK'da kullanıcı adı, parola, API anahtarı, OPDS URL'si veya
kişisel kitap dosyaları bulunmaz. Anahtarları GitHub issue'suna veya ekran
görüntüsüne koyma.

## Test sınırları

Bu sürüm bir deneme yapısıdır. Sunucudaki Komga/Kavita yanıtları kontrol edildi,
ancak fiziksel telefonda oturum açma ve okuma akışı henüz doğrulanmadı.
Uygulama veri yedeği almadan üstüne başka bir imzayla kurulamayabilir.
