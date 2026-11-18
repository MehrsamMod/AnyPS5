[English](../../README.md) | [Português (Brasil)](docs/user/README.pt-BR.md) | [Español](docs/user/README.es.md) | [Català](docs/user/README.ca.md) | [Italiano](docs/user/README.it.md) | [简体中文](docs/user/README.zh-CN.md) | [Русский](docs/user/README.ru.md) | [Bahasa Indonesia](docs/user/README.id.md) | [Polski](docs/user/README.pl.md) | [日本語](docs/user/README.ja.md) | **Türkçe**

# Hakkında

Çalıştırılabilir dosyaların (executable) Linux ve Windows'a otomatik olarak taşınmasını sağlayan bir araç.

Yalnızca "relinker" (yeniden bağlayıcı) içeren sürüm, Apple Silicon dahil olmak üzere macOS üzerinde çalışır.

[**Web dönüştürücü**](https://boykopovar.github.io/AnyPS5/) - dosyalar cihazınızda kalır.

![anyps5_collage1](https://github.com/user-attachments/assets/ed2f0b2d-33d3-46d7-ab88-767ca872fc99)

Çalıştırılabilir dosyaları hedef sistemin yerel biçimine dönüştüren bir [relinker](core/relinker) ve dinamik bağlama için uygun [sistem prx kütüphaneleri](core/libs/prx) uygulamalarını içerir. Emülasyon veya ayrı bir çalışma zamanı (runtime) süreci gerektirmez.

[**Discord**](https://discord.gg/x9naWVzC6A), [Kullanım](docs/user/USAGE.md), [Derleme talimatları](docs/dev/BUILD.md), [Mimari](docs/dev/ARCHITECTURE.md), [Projenin teknik borcu](docs/dev/TechnicalDebt.md), [Kod stili kuralları](docs/dev/CONVENTIONS.md), [Katkıda bulunma](CONTRIBUTING.md)

## Durum

[![kütüphaneler](https://boykopovar.github.io/AnyPS5/badge-libraries.svg)](https://boykopovar.github.io/AnyPS5/progress.html) [![RDNA2 referans gölgelendirici (shader) biçimlerinin kodu çözüldü](https://boykopovar.github.io/AnyPS5/badge-shaders.svg)](https://boykopovar.github.io/AnyPS5/progress.html) [![gfx1013 referans gölgelendirici (shader) biçimlerinin kodu çözüldü](https://boykopovar.github.io/AnyPS5/badge-shaders-gfx1013.svg)](https://boykopovar.github.io/AnyPS5/progress.html) [![7 günde uygulandı](https://boykopovar.github.io/AnyPS5/badge-week.svg)](https://boykopovar.github.io/AnyPS5/history.html)

[![ilerleme haritası](https://boykopovar.github.io/AnyPS5/progress.svg)](https://boykopovar.github.io/AnyPS5/progress.html)

[İlerleme geçmişi](https://boykopovar.github.io/AnyPS5/history.html)

<sub>* Sistem kütüphaneleri: Tüm PS5 sistem işlevlerinin değil, şu ana kadar proje tarafından bilinen ( [core/libs/prx](core/libs/prx) dizininde tanımlanmış) işlevlerin yüzdesidir. Yeni işlevler tanımlandıkça toplam sayı artar.</sub>

Desteklenmeyen veya beklenmedik durumlar, genellikle `std::runtime_error` olmak üzere bir C++ istisnası (exception) fırlatır. Yakalanmayan bir istisna oluştuğunda, istisnanın `what()` çıktısı `stderr` kanalına yazdırılır ve süreç sonlandırılır.

[Gölgelendirici yeniden derleyicisi (shader recompiler)](core/shader/recompiler/Recompiler.cpp), başarılı bir şekilde SPIR-V çıktısı üretir ( `ANYPS5_ENABLE_SPIRV_TOOLS` ile derlendiğinde [Spirv-Tools](3rdparty/SPIRV-Tools) aracılığıyla doğrulanır).

## Uyumluluk

Oyun bazlı durum bilgileri ve test raporları, her bir oyun için ayrı bir başlığın bulunduğu [Game bring-up](https://github.com/boykopovar/AnyPS5/discussions/categories/game-bring-up) tartışma bölümünde yer almaktadır.

## Giriş Eşleme 

Analog çubuklar ve tetik tuşları dahil olmak üzere, SDL ile eşlenmiş oyun kumandaları desteklenmektedir. Klavye ve fare kontrolleri, `anyps5-input.ini` dosyası aracılığıyla yapılandırılabilir. Desteklenen cihazlar ve yapılandırma biçimi hakkında ayrıntılı bilgi için [giriş eşleme](docs/user/INPUT_MAPPING.md) bölümüne bakınız.

## Yasal Uyarı

Bu proje; birlikte çalışabilirlik, araştırma, arşivleme ve uyumluluk amaçlarına yöneliktir. Proje; telif hakkıyla korunan yazılımları, aygıt yazılımlarını (firmware), şifreleme anahtarlarını veya özel (kapalı kaynak) kütüphaneleri içermez, dağıtmaz ya da bunların kullanılmasını gerektirmez. Kullanıcılar, bu projeyle birlikte kullanılan tüm ikili dosyaların (binary), ilgili yasalara ve kendi lisans koşullarına uygun şekilde edinilmesinden ve kullanılmasından kendileri sorumludur.

AnyPS5 bağımsız bir projedir; Sony Interactive Entertainment ile herhangi bir bağlantısı yoktur ve bu şirket tarafından yetkilendirilmemiş veya desteklenmemiştir. "PlayStation" ve "PS5", Sony Interactive Entertainment Inc. şirketinin ticari markalarıdır.

## Lisans

Bu proje, yalnızca GNU Genel Kamu Lisansı (GNU General Public License) sürüm 2 kapsamında lisanslanmıştır.
