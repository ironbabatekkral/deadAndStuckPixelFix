# 🖥️ Dead & Stuck Pixel Fix

Ölü ve sıkışmış pikselleri onarmak için tasarlanmış, tarayıcı tabanlı bir piksel onarım aracı. [JScreenFix](https://www.jscreenfix.com/) projesinden ilham alınmıştır.

> ⚠️ **Uyarı:** Bu araç, sıkışmış (stuck) pikselleri düzeltmeye yardımcı olabilir ancak **sorununuzu kesin olarak çözeceğinin garantisi yoktur**. Ölü (dead) pikseller genellikle donanımsal bir sorun olduğu için yazılımsal yöntemlerle onarılamayabilir. Bu araç bir tavsiye niteliğindedir, profesyonel destek almayı da değerlendirin.

## 🌐 Canlı Demo

🔗 **[Hemen Dene](https://ironbabatekkral.github.io/deadAndStuckPixelFix/)**

## ✨ Özellikler

| Özellik | Açıklama |
|---------|----------|
| ⚠️ **Epilepsi Uyarısı** | Işığa duyarlı kullanıcılar için zorunlu onay ekranı |
| 🎯 **Sürüklenebilir Kare** | Piksel onarıcıyı sorunlu pikselin üzerine sürükleyin |
| 📐 **Boyut Ayarı** | 64px – 512px arası slider ile boyutlandırma |
| ➕ **Çoklu Kare** | 1-6 arası kare ile aynı anda birden fazla pikseli onarın |
| 🚀 **Tam Otomatik Mod** | Özel çözme algoritmaları arasında otomatik geçiş yapar |
| ⚡ **Klasik Mod** | Rastgele RGB piksel flash (JScreenFix algoritması) |
| 🚀 **Hızlı Mod** | Agresif (10ms) piksel stimülasyonu |
| 🌈 **Renk Döngüsü** | Kırmızı → Yeşil → Mavi → Beyaz → Siyah döngüsü |
| ◐ **Siyah-Beyaz** | Yalnızca siyah/beyaz flash |
| 📺 **Karıncalanma** | Eski TV'lerdeki gibi statik siyah-beyaz noise |
| 🔄 **Zıt Renkler** | Kırmızı/Cyan, Yeşil/Magenta, Sarı/Mavi geçişi |
| 🔍 **Piksel Testi** | Yanıp sönme olmadan sabit renklerde ölü piksel arama |
| 🩺 **Teşhis Motoru** | Test modunda hatalı pikseli analiz edip özel tedavi öneren zeka |
| ⏱️ **Zamanlayıcı (Auto-stop)** | 5, 10, 20 veya 60 dk sonra otomatik durdurma |
| 🛡️ **Göz Koruması** | Şiddetli flaşlara karşı göz dinlendiren kehribar arka plan (Amber Modu) |
| 🔲 **Şeffaf Arkaplan (Overlay)**| Sadece onarıcı kareyi bırakıp arkada çalışmaya devam edin |
| 👁️ **Arayüz (UI) Gizleme**| Onarım yaparken dikkat dağıtan tüm menüleri tamamen saklayın |
| 💾 **Otomatik Kayıt** | Sayfa yenilendiğinde ayarlar korunur (localStorage) |
| 🖥️ **Tam Ekran** | Fullscreen API desteği |

## ⌨️ Klavye Kısayolları

| Tuş | İşlev |
|-----|-------|
| `Space` | Duraklat / Devam Et |
| `F` | Tam Ekran |
| `H` | Sağ Üst Paneli Gizle/Göster |
| `T` | **Tüm Kullanıcı Arayüzünü Gizle/Göster** |
| `B` | **Şeffaf Arkaplan Modunu Aç/Kapat (Overlay)** |
| `A` | **Göz Korumasını (Amber Modu) Aç/Kapat** |
| `+` / `-` | Kare Sayısı Artır/Azalt |
| `1`-`8` | Mod Seçimi |

## 🚀 Kullanım

1. [Canlı demo](https://ironbabatekkral.github.io/deadAndStuckPixelFix/) sayfasını açın
2. Piksel onarıcıyı sıkışmış pikselin üzerine sürükleyin
3. En az **10-20 dakika** çalışır durumda bırakın
4. İhtiyaca göre modu ve boyutu ayarlayın

## 🛠️ Yerel Kullanım

```bash
git clone https://github.com/ironbabatekkral/deadAndStuckPixelFix.git
cd deadAndStuckPixelFix
# index.html dosyasını tarayıcınızda açın
```

## 📝 Lisans

Bu proje [MIT Lisansı](LICENSE) ile lisanslanmıştır.

---

## 🔬 İleri Seviye AR-GE ve Teknik Yaklaşım

Bu proje, basit bir renk değiştirme uygulamasından öte, **LCD ve OLED panellerin fiziksel tepkilerini manipüle etmeye yönelik** teknolojik altyapılar içerir.

| AR-GE Başlığı | Teknik Metot | Hedef Sonuç |
| :--- | :--- | :--- |
| **Hertz-Sync (`rAF`)** | `requestAnimationFrame` ile tam Donanım Senkronizasyonu | Frame atlaması olmadan, monitörün native Hz frekansında kesintisiz uyarı silsilesi. |
| **Sub-Pixel Blitz** | Çapraz zıtlıklar üzerinden Complementary Stress | Arızalı alt-pikselin transistörüne maksimum voltaj farkı (0-255 anlık zıplamalar) uygulanması. |
| **Targeted Reset (Expert)** | Mavi/Kırmızı/Yeşil bazlı spesifik zıtlık (Örn: Mavi için Sarı/Siyah) | Bozuk hücreyi kapanmaya (OFF) zorlarken etraftaki komşu renkleri tam yük (255) çalıştırarak voltaj baskısı kurmak. |
| **Voltage Scan** | Sine-Wave (Sinüs Dalgası) Inverse Dithering | Voltajı (parlaklığı) L0 ile L255 arasında yumuşak ama çok hızlı dalgalandırarak kristalin yapışkan (viskoz) direncini kırmak. |
| **Spatial Voltage Pull** | Micro-Shift Checkerboard (Hareketli Dama Tahtası) | Sorunlu pikselin etrafındaki komşu hücreleri her frame'de 1 piksel x/y ekseninde kaydırarak sentetik, titreşimli bir manyetik alan yaratmak. |
| **High-Freq Noise** | Offscreen Caching ile Yüksek Frekanslı Rastgelelik | Statik piksel yapısını kırmak için sürekli değişen voltaj yükü ile kristalin yeniden dizilime zorlanması. |
| **Diagnostic Engine** | İnteraktif Test Modu ve Karar Ağacı | Kullanıcının test esnasında gördüğü hatayı analiz ederek (Dead vs Dormant) en uygun Uzman Tedavisine otomatik yönlendirme yapılması. |
| **Luminance Masking** | Optik Güvenlik Katmanı (Amber Eye-Protection) | Terapinin uzun süreli kesintisiz uygulanabilmesi için göz sağlığını ve epilepsi riskini hafifleten UI tasarımı. |
| **Thermal Pulse** | Panel Isıtma (Dolaylı) | Yüksek parlaklıklı beyaz stres sayesinde lokal fiziksel genleşme yaratılarak kristal hareketini (akışkanlığını) artırma ihtimali. |
