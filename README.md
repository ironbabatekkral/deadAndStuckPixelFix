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
| ⏱️ **Zamanlayıcı (Auto-stop)** | 5, 10, 20 veya 60 dk sonra otomatik durdurma |
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