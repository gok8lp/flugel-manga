# Koharia Reader

Koharia/Mihon tabanlı kişisel Android manga ve kitap okuyucu uyarlaması.
Personal Android reader fork based on [Koharia](https://github.com/Mister-album/Koharia), built on [Mihon](https://github.com/mihonapp/mihon).
Bu depo bu projelerin resmî sürümü değildir; özgün yazarların çalışmaları ve lisansları korunur.

## Ne yapar?

Komga, Kavita ve yerel kitaplık bağlantılarını kullanarak manga ve kitap okuma akışını kişisel sunucu düzenine uyarlar.
Depoda başka sağlayıcılara ait upstream modüller de vardır; modülün bulunması bu uyarlamada uçtan uca doğrulandığı anlamına gelmez.
Kitap, hesap bilgisi veya hazır sunucu erişimi sağlamaz.

## Kullanıcı olarak başlamak

1. Bu deponun [Releases](https://github.com/gok8lp/koharia-reader/releases) bölümünde yayımlanmış bir test APK'si varsa sürüm notlarını oku.
2. Uygulamada kendi Komga/Kavita sunucunu ve hesabını yapılandır.
3. Bağlantı, kitaplık görünümü ve okuma akışını kendi cihazında dene.

Ayrıntılı adımlar: [Android kurulum notları](ANDROID_SETUP.md).
Önceki test APK'leri eski uygulama adını taşıyabilir; kaynak değişikliği mevcut APK'yi yeniden derlemez.

## Kaynaktan derleme

Android Studio, projenin Android SDK/NDK bileşenleri ve Gradle için Java 17 gerekir.
Kesin sürümler `gradle/koharia.versions.toml`, `.github/.java-version` ve build dosyalarında tanımlıdır.

```bash
./gradlew spotlessCheck
./gradlew :app:compileDebugKotlin
./gradlew :app:assembleDebug
```

Windows'ta aynı görevler `gradlew.bat` ile çalıştırılır. APK'ler `app/build/outputs/apk/` altında oluşur.
Yayın imzalama anahtarları depoya eklenmez; debug APK geliştirme içindir.

## Proje haritası

| Dizin | İçerik |
| --- | --- |
| `app/` | Android uygulaması, ekranlar ve bağlantı yönetimi |
| `i18n/` | Ortak ve Türkçe metin kaynakları |
| `data/`, `domain/` | Veri ve iş kuralları |
| `core/`, `presentation-*` | Ortak altyapı ve arayüz bileşenleri |
| `.github/workflows/` | Derleme ve doğrulama iş akışları |

## Kaynak ve lisans

Upstream açıklamalar: [English](README_EN.md) · [简体中文](README_UPSTREAM.zh-CN.md).
Bu belgelerdeki upstream indirme ve destek bağlantıları özgün projeye aittir.
[LICENSE](LICENSE), [NOTICE](NOTICE), [CONTRIBUTING.md](CONTRIBUTING.md) ve üçüncü taraf atıfları korunmuştur.
Koharia, Mihon, Komga veya Kavita'nın resmî ürünü olduğu iddia edilmez.
